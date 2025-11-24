# 📄 Project Statement: Tech Shop CLI Shopping Cart

## I. Problem Statement 🎯

The challenge is to implement a **functional simulation of an e-commerce shopping cart** using fundamental **Python programming constructs**. This requires modeling product data, managing dynamic user selections (the cart), performing financial calculations (subtotal, tax, total), and providing a stable, interactive command-line interface (CLI) for user interaction. The project must demonstrate proficiency in data structuring, function modularity, and error handling in a procedural environment.

---

## II. Scope of the Project 🔭

The project scope is strictly limited to the **backend logic and front-end CLI interaction** of a shopping cart system.

### Inclusions:
* **Core CRUD Logic for Cart:** Ability to Add (Create) items to the cart and Read (View) the cart contents.
* **Financial Processing:** Calculation of line totals, subtotal, sales tax (7% fixed rate), and final total.
* **Input Validation:** Basic error handling for invalid data types or out-of-range inputs (e.g., non-numeric IDs, negative quantities).
* **Session Management:** The cart persists as long as the application is running and is cleared upon a confirmed checkout.

### Exclusions:
* **Database Integration:** Data (catalog, cart) is stored only in in-memory Python dictionaries.
* **Persistence:** The cart data is **not saved** between application runs.
* **Advanced Features:** No user authentication, payment gateway integration, shipping calculation, inventory tracking, or item removal/modification features.
* **Graphical User Interface (GUI):** All interaction occurs via the command line.

---

## III. Target Users 👤

The primary target audience for this project falls into two categories:

1.  **Students/Learners of Python:** Individuals studying basic data structures (dictionaries), control flow, and function definition. The project serves as a clear, working example of how to combine these concepts into a complete application.
2.  **Portfolio Reviewers/Hiring Managers:** Individuals assessing the developer's foundational skills in clean, modular Python coding, logic implementation, and practical application development using only native tools.

---

## IV. High-Level Features ✨

| Feature Category | Description | Implementation Details |
| :--- | :--- | :--- |
| **Catalog Access** | Allows users to see all products, prices, and Item IDs available in the store. | `display_products()` function reading from `PRODUCT_CATALOG`. |
| **Cart Manipulation** | Enables users to add specific items and quantities to their shopping cart. | `add_to_cart()` function modifies the global `shopping_cart` dictionary. |
| **Cart Visualization** | Displays the current contents of the cart with comprehensive details. | `view_cart()` function calculates line totals and the subtotal. |
| **Financial Summary** | Calculates the final cost including tax before purchase confirmation. | `checkout()` function applies the fixed `TAX_RATE` to the subtotal. |
| **Application Flow** | Provides a structured, looping menu system for navigating between features. | `main_menu()` and the `main()` application loop. |
