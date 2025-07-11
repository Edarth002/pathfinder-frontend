**"Design and Implementation of a Campus Navigation System Using Graph-Based Pathfinding and Location Data"**s

---

````markdown
# 🧭 Intelligent Campus Navigation System

This is a full-stack application(Frontend Part) for pedestrian navigation on university campuses, tailored for the University of Nigeria, Nsukka (UNN). It combines an intelligent pathfinding algorithm with geospatial data and user preferences to guide students, staff, and visitors efficiently.

---

## 📌 Project Title

**Design and Implementation of a Campus Navigation System Using Graph-Based Pathfinding and Location Data**

---

## 🛠 Tech Stack

- **Backend**: Node.js, Express.js
- **Database**: MySQL (or PostgreSQL)
- **Authentication (optional)**: JWT
- **Mapping Tools**: Leaflet.js / Mapbox GL JS / OpenLayers
- **Pathfinding Algorithm**: A\* (A-star) or Dijkstra’s algorithm
- **Hosting**: Railway (backend)

---

## 📁 Folder Structure

```bash
.
├── backend/
│   ├── controllers/
│   ├── models/
│   ├── routes/
│   ├── utils/              # pathfinding logic here
│   ├── config/
│   └── server.js
├── frontend/
│   ├── components/
│   ├── pages/ or src/
│   ├── services/
│   └── App.js / layout.tsx
├── .env
└── README.md
```
````

---

## 🎯 Features

- Interactive campus map for route planning
- Personalization using user preferences (e.g., shortest, most accessible)
- Clean, mobile-responsive frontend
- Easy to extend for other institutions

---

## 🔌 Backend API Endpoints

| METHOD | ENDPOINT               | DESCRIPTION                                           |
| ------ | ---------------------- | ----------------------------------------------------- |
| GET    | `/api/locations`       | Fetch all campus locations                            |
| GET    | `/api/paths`           | Retrieve path connections between locations           |
| POST   | `/api/find-best-route` | Get optimal path based on input, and user preferences |

---

## 🚀 Installation Guide

### 1. Clone the Repository

```bash
git clone https://github.com/edarth002/pathfinder-api.git
```

### 2. Setup Backend

```bash
cd pathfinder-api
npm install
```

**.env example:**

```env
PORT=5000
DB_HOST=localhost
DB_USER=root
DB_PASS=yourpassword
DB_NAME=campus_nav
JWT_SECRET=your_jwt_secret
```

Then start the server:

```bash
npm run dev
```

## 🗺️ How the Pathfinding Works

1. All campus locations are stored as **nodes**.
2. Paths (edges) connect them, with weights for distance, accessibility, and other metrics.
3. A\* or Dijkstra’s algorithm is applied based on weights and preferences.
4. The algorithm returns the **most optimized route**, which is rendered on a map.

Example preference impact:

- "Avoid stairs": increases weights of stair-connected paths
- "Prefer shaded": reduces weights of tree-lined paths

---

## 🧪 Sample Data Schema

### `locations` Table

| id  | name             | type     | lat    | lng    |
| --- | ---------------- | -------- | ------ | ------ |
| 1   | Faculty of Engr. | building | 6.8521 | 7.4033 |

### `paths` Table

| id  | from_node | to_node | distance | has_stairs | is_shaded |
| --- | --------- | ------- | -------- | ---------- | --------- |

---

## 📚 Academic Relevance

This project directly supports:

- **UN SDG 9**: Industry, Innovation, and Infrastructure
- **UN SDG 11**: Sustainable Cities and Communities

It was developed as part of a BSc project in Computer Science, University of Nigeria, Nsukka.

---

## 📖 License

MIT © 2025 Arthur Onyeanusi

---

## 📞 Contact

- Email: [arthuronyeanusi@gmail.com](mailto:arthuronyeanusi@gmail.com)
- GitHub: [github.com/edarth002](https://github.com/edarth002)
- LinkedIn: [linkedin.com/in/your-profile](https://linkedin.com/in/your-profile)

