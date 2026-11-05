# Digital Wallet (JavaFX)

Desktop digital wallet built with **Java** and **JavaFX**. Users sign in, manage their bank accounts, make deposits, withdrawals and transfers, and review their transactions. An administrator view manages registered users.

Final project for **Programación II**, Systems Engineering, Universidad del Quindío (May 2025).

## Objective

Apply object-oriented design to a complete desktop application: layered packages, service interfaces, design patterns and an FXML-based user interface.

## Technologies

- Java (JPMS module: `module-info.java`)
- JavaFX 23 (`javafx-controls`, `javafx-fxml`) with FXML views
- Maven project layout
- Patterns: Builder (`UsuarioBuilder`, `TransaccionBuilder`), a factory/controller entry point to the model (`ModelFactoryController`), and service interfaces

## Main features

- User registration and sign-in
- Account management per user (bank and account type)
- Deposits, withdrawals and transfers between accounts
- Transaction history with filters by category, date range and type
- User settings (update and delete profile)
- Administrator view for user management
- Service layer for categories, budgets and statistics (users with most transactions, average balance, most common expenses)

Data is kept in memory while the application runs.

## Project structure

```text
src/main/java/co/edu/uniquindio/poo/billeteradigital/
├── LanzarAplicacion.java     # JavaFX entry point
├── controller/               # Application controllers
├── enums/                    # Bank, account and transaction types
├── factory/                  # ModelFactoryController
├── interfaces/               # Service contracts
├── model/                    # User, Account, Transaction, Category, Budget (+ builders)
├── service/                  # Business logic
├── utils/                    # Validation and message constants
└── viewcontroller/           # FXML controllers (user, admin, forms)
src/main/resources/
├── views/                    # FXML views
└── images/
```

## Requirements

- JDK 21 or later (required by JavaFX 23)
- JavaFX 23 (downloaded by Maven or configured in the IDE)
- IntelliJ IDEA (recommended)

## Running

1. Clone the repository and open it in IntelliJ IDEA as a Maven project.
2. Run `co.edu.uniquindio.poo.billeteradigital.LanzarAplicacion`.

> **Note:** the current `pom.xml` only contains the `<dependencies>` block (it was reduced in the commit "actualizacion en pom.ml"). The complete version from the first commit includes the compiler and `javafx-maven-plugin` configuration needed to build from the command line.

## Project status

Delivered as the course final project. No automated tests yet.
