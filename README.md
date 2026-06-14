# Bank Theft Detection System (BTDS)

A C++ console application that simulates a secure banking system with real-time fraud detection using Object-Oriented Programming concepts.

---

## Features

- Secure PIN-based login with account lockout after 3 failed attempts
- Fraud detection for suspicious transactions (large amounts, unusual locations, night-time activity)
- Daily withdrawal limit enforcement
- Custom exception handling for all fraud and error scenarios
- Multi-level inheritance: Account → SavingAccount → HighSecurityAccount

---

## OOP Concepts Used

| Concept | Where Used |
|---|---|
| Inheritance | Account → SavingAccount → HighSecurityAccount |
| Polymorphism | `withdraw()` and `showInfo()` overridden in derived classes |
| Encapsulation | Private data members (balance, PIN) with public methods |
| Exception Handling | Custom `FraudException` class |
| Function Overloading | `SecurityEngine::detect()` with 3 versions |
| Static Members | `Account::totalAccounts` |

---

## How to Run

**Compile:**
```
g++ BTDS_project_.cpp -o btds
```

**Run:**
```
./btds
```

---

## Fraud Detection Rules

- Amount over 100,000 → flagged as suspicious
- Amount over 50,000 from unknown location → flagged
- Any transaction between 12am–5am from unknown location → flagged
- Withdrawal over daily limit (80,000) → blocked
- 3 wrong PIN attempts → account locked

---

## Sample Usage

```
=== Bank Theft Detection System (BTDS) ===
1. Login
2. Withdraw (simulate transaction)
3. Show Account Info
0. Exit
```

---

## Technologies

- Language: C++
- Concepts: OOP, Custom Exceptions, Polymorphism, Inheritance

---

## Author

Made as a university project demonstrating core C++ OOP and security concepts.
