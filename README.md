# 🍽️ Meal Maker
Creates a simple restaurant “Today’s Special” system using **getters** and **setters** so staff can set a meal and a price safely, then display the special without embarrassing errors.

- Holds private-like fields for **meal** and **price**
- Validates inputs (meal → string, price → number)
- Provides a getter to show **Today’s Special**

---

### 💻 Code
```javascript


const menu = {
  _meal: '',
  _price: 0,

  // Validate & set meal (must be a non-empty string)
  set meal(mealToCheck) {
    if (typeof mealToCheck === 'string' && mealToCheck.trim()) {
      this._meal = mealToCheck.trim();
    }
  },

  // Validate & set price (must be a non-negative number)
  set price(priceToCheck) {
    const n = Number(priceToCheck);
    if (Number.isFinite(n) && n >= 0) {
      this._price = n;
    }
  },

  // Show today's special if both values are set
  get todaysSpecial() {
    if (this._meal && this._price) {
      return `Today's Meal is ${this._meal} for $${this._price}!`;
    } else {
      return 'Meal or price was not set correctly!';
    }
  }
};


---
```

### 📦 Example Output
```
Meal : chicken
Price : $9
Today's Meal is chicken for $9!
```

---

### 🎯 Skills Learned
- Creating objects with getters and setters
- Input validation and safe assignment
- Conditional logic to guard outputs
- Basic Node.js script execution


- Array `push()` method
- Joining arrays into strings and converting to uppercase
