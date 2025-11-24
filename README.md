
# 🛒 Tech Shop CLI - Python Shopping Cart Application

## 💡 Project Title
**Tech Shop Command-Line Interface (CLI) Shopping Cart**



## 📄 Overview of the Project
This is a simple, console-based application built entirely in **Python**. It simulates the fundamental operations of an e-commerce shopping cart system. The user can interact with a pre-defined product catalog, add items to a virtual cart, view the running totals, and proceed through a basic checkout process that includes sales tax calculation. It's an excellent example of basic data management using Python dictionaries and procedural logic.



## ✨ Features
* **Product Catalog Management:** Stores product data (ID, name, price) in a Python dictionary (`PRODUCT_CATALOG`).
* **Interactive Menu:** Provides a clear, numbered menu for navigation.
* **Add/Update Cart:** Allows users to select items by ID and add quantities. If an item is already in the cart, its quantity is updated.
* **Detailed Cart View:** Displays the quantity, item name, unit price, and calculates the **line total** for each item.
* **Subtotal Calculation:** Automatically calculates the total cost before tax.
* **Checkout & Tax:** Applies a **7% fixed sales tax** (`TAX_RATE = 0.07`) to the subtotal to determine the final amount due.
* **Order Confirmation:** Clears the cart only after the user confirms the final purchase.
* **Robust Input Handling:** Includes basic `try-except` blocks to handle non-numeric or invalid ID inputs gracefully.



## 🛠️ Technologies/Tools Used
* **Language:** Python 3 (specifically Python 3.6+)
* **External Libraries:** None (The project uses only **built-in Python features** and the `sys` module for clean exit).
* **Environment:** Command-Line Interface (CLI)



## 🚀 Steps to Install & Run the Project

### Prerequisites

You must have **Python 3** installed on your system. You can check your version by running:

bash
python --version
# or
python3 --version


### Installation and Execution

1.  **Save the Code:** Save the entire provided Python script into a file named `shopping_cart.py`.

2.  **Navigate:** Open your terminal or command prompt and change the directory to where you saved the file.

    ```bash
    cd /path/to/your/project
    ```

3.  **Run the Application:** Execute the script using the Python interpreter.

    ```bash
    python shopping_cart.py
    ```

4.  **Start Shopping\!** The main menu will be displayed, and you can begin interacting with the application.

-----

## 🧪 Instructions for Testing

Follow these steps to thoroughly test the application's core functionality:

1.  **Test Case 1: Initial View**
      * Select **1** (View Products).
      * *Expected Result:* All 5 products from the `PRODUCT_CATALOG` are displayed clearly.
2.  **Test Case 2: Adding and Updating Items**
      * Select **2** (Add Item to Cart).
      * Enter ID: `1` (Laptop), Quantity: `1`.
      * Select **2** again.
      * Enter ID: `1` (Laptop), Quantity: `2`.
      * Select **3** (View Shopping Cart).
      * *Expected Result:* The cart shows the Laptop item with a **Quantity of 3** (1 + 2).
3.  **Test Case 3: Empty Cart Checkout**
      * Ensure the cart is empty (if you just ran Test Case 2, skip this step and clear the cart manually or restart the script).
      * Select **4** (Checkout).
      * *Expected Result:* A message appears: "Cannot checkout with an empty cart."
4.  **Test Case 4: Full Checkout Process**
      * Add an item, e.g., ID `2` (Mechanical Keyboard), Quantity `1`.
      * Select **4** (Checkout).
      * *Expected Result:* The **Subtotal** is $75.50. **Tax (7.0%)** is calculated as $5.29. **Total** is $80.79.
      * Enter `yes` to confirm.
      * *Expected Result:* The cart is cleared.
5.  **Test Case 5: Input Validation**
      * Select **2** (Add Item to Cart).
      * Enter ID: `hello` (non-numeric).
      * *Expected Result:* Prints "Invalid input..."
      * Enter ID: `99` (invalid ID).
      * *Expected Result:* Prints "Invalid item ID..."
      * Enter ID: `1`, Quantity: `-5` (invalid quantity).
      * *Expected Result:* Prints "Quantity must be greater than zero."



