# 🥘 British Meals Explorer (React + MealDB)

A simple and dynamic React application that displays a collection of **British cuisine meals** using the [MealDB API](https://www.themealdb.com/api.php). It offers a "Show More" feature to explore meals gradually for better UX.

---

## ✅ Description

> A simple React app that fetches and displays British meals from the MealDB API with a dynamic "show more" feature.

---

## ⚙️ Features

- 🇬🇧 Fetches **British meals** from the MealDB API  
- 📷 Displays meal images and names in a card layout  
- ➕ “Show More” button to load meals incrementally  
- ⚛️ Built with functional React components and hooks  
- 🎨 Responsive layout with minimal styling

---

## 🧠 How It Works

- Uses `useEffect` to fetch meals on first render:

```js
useEffect(() => {
  fetch("https://www.themealdb.com/api/json/v1/1/filter.php?a=british")
    .then((res) => res.json())
    .then((data) => setItems(data.meals));
}, []);
