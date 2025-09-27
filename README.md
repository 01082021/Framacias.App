/* Reset y básicos */
* { box-sizing: border-box; }
body {
  margin: 0;
  font-family: Arial, sans-serif;
  background: white

}

/* Navbar */
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background: #457b2c;
  padding: 1rem 2rem;
  color: white;
}
.brand { margin: 0; }
.nav-links {
  display: flex;
  list-style: none;
  gap: 1rem;
  margin: 0;
  padding: 0;
}
.nav-links a {
  color: white;
  text-decoration: none;
  font-weight: bold;
}

/* Footer */
.footer {

 
  text-align: center;
  padding: 0.5rem;
  background: #457b2c;
  color: white;
  font-size: 0.9rem;
}


/* Páginas */
.home, .medicamentos, .contacto {
  padding: 2rem;
  max-width: 1000px;
  margin: 0 auto;
  text-align: center;
}

/* Buscador y grid */
.search {
  padding: 0.6rem;
  width: 100%;
  max-width: 400px;
  margin: 1rem auto;
  border-radius: 6px;
  border: 1px solid black;
}
.grid {
  display: flex;
  flex-wrap: wrap;
  gap: 1rem;
  justify-content: center;
  margin-top: 1rem;
}

/* Card */
.card {
  background: white;
  padding: 1rem;
  border: 1px solid greenyellow;
  border-radius: 20px;
  width: 220px;
  box-shadow: 2px 2px 6px rgba(0,0,0,0.06);
}
.card h3 { margin: 0 0 0.5rem 0; color: #457b2c; }

/* Contacto form */
.contacto form {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  max-width: 500px;
  margin: auto;
}
.contacto input, .contacto textarea {
  padding: 0.7rem;
  border: 1px solid white;
  border-radius: 5px;
  font-size: 1rem;
}
.contacto button {
  padding: 0.7rem;
  background: #457b2c;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}
.contacto button:hover { background: #457b2c; }

/* Responsive */
@media (max-width: 400px) {
  .nav-links { display: none; } 
  .card { width: 100%; max-width: 320px; }
}


import { Routes, Route } from "react-router-dom";
import Navbar from "./components/Navbar";
import Footer from "./components/footer";
import Home from "./pages/home";
import Medicamentos from "./pages/medicamentos";
import Contacto from "./pages/contacto";

function App() {
  return (
    <div className="App">
      {/* Barra de navegación */}
      <Navbar />

      {/* Contenido principal con rutas */}
      <main style={{ paddingBottom: "4rem" }}>
        <Routes>
          <Route path="/" element={<Home />} />
          <Route path="/medicamentos" element={<Medicamentos />} />
          <Route path="/contacto" element={<Contacto />} />
        </Routes>
      </main>

      {/* Pie de página */}
      <Footer />
    </div>
  );
}

export default App;


body {
  margin: 0;
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Roboto', 'Oxygen',
    'Ubuntu', 'Cantarell', 'Fira Sans', 'Droid Sans', 'Helvetica Neue',
    sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

code {
  font-family: source-code-pro, Menlo, Monaco, Consolas, 'Courier New',
    monospace;
}


import React from "react";
import ReactDOM from "react-dom/client";
import { BrowserRouter } from "react-router-dom";
import App from "./App";
import "./App.css";

const root = ReactDOM.createRoot(document.getElementById("root"));
root.render(
  <BrowserRouter>
    <App />
  </BrowserRouter>
);
