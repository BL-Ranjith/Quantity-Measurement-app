# Quantity Measurement Application 

A comprehensive, test-driven Java application built using Spring Boot that handles quantity measurements, conversions, and arithmetic operations across various physical units (Length, Weight, Volume, and Temperature).

The application is structured following clean coding standards, Test-Driven Development (TDD) principles, and a modern N-Tier Enterprise Architecture.

---

## 🚀 Key Features & Use Cases

### 📏 1. Length Measurement (UC1 - UC8)
- **UC1**: Feet Equality (comparing feet to feet measurements).
- **UC2**: Feet to Inches Equality & Conversion (e.g. \(1 \text{ ft} = 12 \text{ in}\)).
- **UC3**: Generic Quantity representations for length measurements.
- **UC4**: Extended Unit Support (Inches, Feet, Yards, and Miles).
  - \(1 \text{ yd} = 3 \text{ ft}\)
  - \(1 \text{ mile} = 1760 \text{ yd}\)
- **UC5**: Validation of conversions between various length units.
- **UC6**: Addition of Length Units (e.g. \(2 \text{ in} + 2 \text{ in} = 4 \text{ in}\), \(1 \text{ ft} + 2 \text{ in} = 14 \text{ in}\)).
- **UC7**: Addition with unit conversion and custom target output units.
- **UC8**: Centralized conversion factors within a consolidated `Unit` Enum.

### ⚖️ 2. Weight & Volume Measurement (UC9 - UC11)
- **UC9**: Weight Equality & Conversion support for Grams, Kilograms, and Tonnes.
  - \(1 \text{ kg} = 1000 \text{ g}\)
  - \(1 \text{ Tonne} = 1000 \text{ kg}\)
- **UC10**: Generic representation of units for Weight measurements.
- **UC11**: Volume Equality & Conversion support for Gallon, Litre, and Millilitre.
  - \(1 \text{ Gallon} = 3.78 \text{ Litres}\)
  - \(1 \text{ Litre} = 1000 \text{ Millilitres}\)

### ➕ 3. Arithmetic Operations (UC12 - UC13)
- **UC12**: Subtraction and division support between compatible units.
- **UC13**: Centralized Arithmetic service handling calculations across different unit categories with auto-conversion.

### 🌡️ 4. Temperature Measurement (UC14)
- **UC14**: Temperature scale comparison and conversions supporting Fahrenheit (\(^{\circ}\text{F}\)) and Celsius (\(^{\circ}\text{C}\)).
  - Formula: \(F = C \times \frac{9}{5} + 32\)

### 🏛️ 5. Enterprise N-Tier Architecture (UC15 - UC17)
- **UC15**: Restructured application using N-Tier Architecture:
  - **Controller Layer**: Exposes RESTful APIs for client interactions.
  - **Service Layer**: Implements business rules and measurement calculations.
  - **Repository Layer**: Manages persistence operations.
- **UC16**: Database integration to log conversion history and maintain records.
- **UC17**: Spring Boot integration enabling dependency injection, auto-configuration, and API endpoints.

---

## 🛠️ Technology Stack
- **Language**: Java 11/17
- **Framework**: Spring Boot (Spring Web, Spring Data JPA)
- **Testing**: JUnit 5, Mockito (following TDD methodology)
- **Build Tool**: Maven
- **Database**: H2 / MySQL

---

## 📂 Project Structure

Development code and unit tests are organized inside the respective development branches (e.g., `feature-UC0-project-setup` to `feature-UC17-spring-integration`). 

The standard layout of the codebase in development branches:
```text
src/
├── main/
│   ├── java/com/apps/quantitymeasurement/
│   │   ├── controller/      # REST API Controllers
│   │   ├── Service/         # Business Logic / Conversion Services
│   │   ├── repository/      # JPA Repositories
│   │   ├── exception/       # Custom Exception Handlers
│   │   └── Model/           # Entity, Enums and DTOs
│   └── resources/
│       └── application.properties
└── test/                    # JUnit and Mockito Tests
```

---

## 🚦 Getting Started (Development Branches)

To view, run, or test the code, check out any of the specific feature branches:
```bash
git checkout feature-UC17-spring-integration
```

### Run Tests
```bash
mvn test
```

### Run Server
```bash
mvn spring-boot:run
```
