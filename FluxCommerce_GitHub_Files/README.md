# 🛒 FluxCommerce

FluxCommerce is a **console-based e-commerce system written in C** that supports
user registration, authentication, wallet management, product listings,
searching, and transactions between buyers and sellers.

This project demonstrates **file handling, struct usage, validation logic,
and transaction consistency** using pure C.

---

## ✨ Features

### 👤 User System
- Register with strict **username & password validation**
- Case-insensitive usernames
- Login authentication
- Roles:
  - Buyer
  - Seller

### 💰 Wallet System
- Secure top-up with overflow protection
- Persistent balance storage
- Automatic wallet updates after transactions

### 📦 Product System
- Sellers can add products
- Products use **Snowflake-style unique IDs**
- View all products (sorted by ID)
- Search products (case-insensitive)
- Sellers can view only their own products

### 🛍️ Transaction System
- Buyers can purchase products
- Stock validation
- Wallet balance validation
- Seller automatically receives payment
- Transaction history:
  - Buyer history
  - Seller sales history

---

## 🧠 Technical Highlights

- Written in **pure C (C99 compatible)**
- Uses `struct` for User and Product models
- File-based persistence (`.txt` files)
- Manual numeric parsing to prevent overflow
- Case-insensitive search implementation
- Snowflake-style ID generation using timestamp + sequence

---

## 📁 Project Structure

```
FluxCommerce/
│
├── src/
│   └── flux_commerce.c
│
├── data/
│   ├── users.txt
│   ├── products.txt
│   └── transactions.txt
│
├── .gitignore
└── README.md
```

---

## ⚙️ Compilation & Running

### Compile
```bash
gcc src/flux_commerce.c -o flux
```

### Run
```bash
./flux
```

---

## 📄 Data Files

| File | Purpose |
|-----|--------|
| users.txt | User credentials & wallet |
| products.txt | Product listings |
| transactions.txt | Purchase history |

---

## 👨‍💻 Author
FluxCommerce — Built with ❤️ using C
