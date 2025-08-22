package org.example.handlingformsubmission;

// Greeting.java represents the data model for the greeting form.
// It holds the user's input: student ID, message, and date (month, day, year).
public class Greeting {

    private Long id;
    private String content;
    private Integer month;
    private Integer day;
    private Integer year;

    // Getters and setters
    public Long getId() {
        return id;
    }

    public void setId(Long id) {
        this.id = id;
    }

    public String getContent() {
        return content;
    }

    public void setContent(String content) {
        this.content = content;
    }

    // New fields: month, day, year
    public Integer getMonth() {
        return month;
    }

    public void setMonth(Integer month) {
        this.month = month;
    }

    public Integer getDay() {
        return day;
    }

    public void setDay(Integer day) {
        this.day = day;
    }

    public Integer getYear() {
        return year;
    }

    public void setYear(Integer year) {
        this.year = year;
    }
}
