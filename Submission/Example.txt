package org.example;

import org.springframework.boot.*;
import org.springframework.boot.autoconfigure.*;
import org.springframework.web.bind.annotation.*;

/*
Name: Joao Lotfi Barrera
Course: COP-3330C-33777
Date: 07/15/2025

Program Objective:
A Spring Boot web app that accepts user input (Student ID, message, and a date) in a form format,
validates it, and displays the result using Thymeleaf.

Inputs:
- Student ID (number)
- Message (text)
- Month, Day, Year (numbers)

Output:
- Displays submitted data in formatted form on a results page.
*/

// Example.java is used to initialize the Spring Application
// and also returns hello world to the index page.
@SpringBootApplication
@RestController
public class Example {

    @RequestMapping("/")
    String home() {
        return "Hello World!";
    }

    public static void main(String[] args) {
        SpringApplication.run(Example.class, args);
    }
}