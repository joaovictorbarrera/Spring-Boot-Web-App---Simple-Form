package org.example.handlingformsubmission;

import org.springframework.stereotype.Controller;
import org.springframework.ui.Model;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.ModelAttribute;
import org.springframework.web.bind.annotation.PostMapping;

import java.time.DateTimeException;
import java.time.LocalDate;

// GreetingController.java is a controller that handles HTTP requests related to the greeting form.
@Controller
public class GreetingController {

    // GET: /greeting
    // Handles rendering the form while attaching an instance of Greeting to the model
    @GetMapping("/greeting")
    public String greetingForm(Model model) {
        model.addAttribute("greeting", new Greeting());
        return "greeting";
    }

    // POST: /greeting
    // Receives form data and attempts to create a valid date with input
    // Sends back error if date is invalid
    @PostMapping("/greeting")
    public String greetingSubmit(@ModelAttribute Greeting greeting, Model model) {
        model.addAttribute("greeting", greeting);

        try {
            LocalDate date = LocalDate.of(greeting.getYear(), greeting.getMonth(), greeting.getDay());
            model.addAttribute("formattedDate", date);
        } catch (DateTimeException e) {
            model.addAttribute("error", "Invalid date entered. Please try again.");
            return "greeting";
        }

        return "result";
    }
}