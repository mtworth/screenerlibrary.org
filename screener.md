# Food Security Screener Design Document

## 1. Introduction

This document outlines the design for a simple static website that functions as a food security screener. The goal is to provide users with a tool to assess their food security status based on a series of questions.

## 2. Technology Stack

*   **HTML:** For the structure and content of the web pages.
*   **Alpine.js:** For client-side interactivity, such as form handling and displaying results.
*   **CSS:** For styling the website (details to be determined).

## 3. Pages

The website will consist of the following pages:

### 3.1. Landing Page (`index.html`)

*   **Purpose:** To welcome the user, provide a brief explanation of food security, and direct them to the different screening tools.
*   **Content:**
    *   A title and a short introductory text.
    *   Brief descriptions of the available screeners (2-item, 6-item, and 18-item).
*   **Navigation:**
    *   Links to each of the three screener pages.

### 3.2. Screener Pages

There will be three separate screener pages:

*   `screener-2-item.html`
*   `screener-6-item.html`
*   `screener-18-item.html`

Each screener page will have the following components:

*   **Purpose:** To present the user with a specific set of questions to determine their food security status.
*   **Content:**
    *   A form containing the questions for the respective screener.
    *   Each question will have a set of possible answers (e.g., yes/no, often/sometimes/never).
*   **Functionality (Alpine.js):**
    *   An Alpine.js component will manage the state of the form.
    *   A "Submit" or "Calculate" button will trigger the scoring logic.
    *   Upon submission, the form will be processed, and the user's food security status will be calculated.
    *   The result will be displayed on the same page, below the form.

## 4. Food Security Status Calculation

The logic for calculating the food security status will be implemented within Alpine.js on each screener page. The calculation will be based on the user's responses to the questions. The final status (e.g., "High Food Security," "Marginal Food Security," "Low Food Security," "Very Low Food Security") will be displayed to the user.

## 5. File Structure

The project will have a simple file structure:

```
/
|-- index.html
|-- screener-2-item.html
|-- screener-6-item.html
|-- screener-18-item.html
|-- css/
|   `-- style.css
`-- js/
    `-- app.js
```
