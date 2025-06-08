# 🎟️ Cinema Ticketing System – C++ Project Documentation
## Overview
This program is a console-based cinema ticketing system designed to simulate the process of purchasing movie tickets, selecting seats, adding snacks, calculating total payment (including discounts), and generating a printable receipt. It emphasizes logical control flow, user input validation, data handling, and basic file I/O operations.

## 💡 Key Features
Movie and Time Selection: Offers a list of movies with different genres and pricing. Users select their preferred show and time slot.

Seat Selection: Displays a seat map (5x8 grid) and allows users to choose available seats interactively.

Snack Selection: Provides optional condiment sets with associated pricing.

Discount System: Applies automated discounts (10% for students, 50% for children) based on user input.

Multiple Payment Modes: Supports both cash and card payments, including basic card input simulation.

Receipt Generation: Displays and writes a detailed receipt to a .txt file for record-keeping.

## 📁 Functional Breakdown
Main Function Flow
int main();
Orchestrates the program's flow:

- Registers members (optional)

- Displays welcome screen

- Handles user choices for movies, time, seats, and snacks

- Applies discounts

- Manages payment processing

- Collects user info and generates the receipt (both display and file output)

## 📦 Core Modules and Their Roles
void displayWelcome()
Displays an introductory message and instructions.

char chooseMovie(char k)
Outputs a list of movies and returns a character to signal selected movie.

int chooseTime(int c)
Presents available showtimes based on selected movie.

void chooseSeat()
Visual interface to select and reserve seats within a matrix. Ensures no seat is double-booked.

int count_seat()
Tracks and returns the number of tickets purchased.

double chooseCondiment()
Allows selection of snack combos (Set A, B, or C). Computes and returns the total snack cost.

double checkAge(double x, int st, int ch)
Applies discount logic:

10% for students

50% for children
Discounts are dynamically computed based on ticket price and returned for deduction from total payment.

double totalPrice(int movie, int count, double snackCost)
Combines ticket and snack pricing to calculate the gross total.

double payment(double amount)
Handles payment logic. Accepts both cash and simulated card input. Manages balance and enforces sufficient payment.

int Printreceipt(...)
Displays ticket receipt with full details: movie, time, user, contact, seat info, total paid.

int PrintableReceipt(...)
Exports the same receipt to a .txt file for external use (e.g., printing or emailing).

## 🧠 Concepts Demonstrated
Conditional Logic: Structured if, switch, and loop constructs to control user flow.

Data Validation: Prevents duplicate seat selection and insufficient payment.

Basic OOP Practices: Modular decomposition using functions for maintainability.

User Experience (UX): Clear prompts, error handling, and aesthetic seat map display.

File Handling: Outputs transaction summary to a file via ofstream.

Mathematical Computation: Total price calculations, discounting, and change calculation.

## 💻 Technologies Used
Language: C++

Standard Libraries: <iostream>, <fstream>, <iomanip>, <string.h>, <cstdlib>, <ctime>, <conio.h>

## ✅ Potential Use Cases
Cinema Simulation Systems

Ticketing Kiosk Prototype

Basic POS System

Learning Tool for Input Processing, File I/O, and Pricing Logic

## 📈 Application to a Data/Software Analyst Role
This project demonstrates:

Clear understanding of structured logic

Ability to build a user-oriented system

Capability to process input/output efficiently

Implementation of pricing logic and conditional discounts

Use of file output for reporting — akin to automated reporting scripts or data export logic used in real-world analytics tools
