# <img src="https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/pokemon/25.png" width="30" height="30"> JavaScript Pokédex

[![Live Demo](https://img.shields.io/badge/Play%20Now-Online-brightgreen)](https://munique-feitoza.github.io/pokedex_in_js/)
![GitHub last commit](https://img.shields.io/github/last-commit/Munique-Feitoza/pokedex_in_js)

An interactive Pokédex built with vanilla JavaScript that fetches data from PokeAPI to display Pokémon information.

![Pokédex Screenshot](https://github.com/Munique-Feitoza/pokedex_in_js/assets/140446097/0dd88897-001b-467a-bda6-9a299e4d194a)

## ✨ Features

- **Search functionality** by name or ID
- **Detailed Pokémon info**: types, abilities, stats
- **Animated sprites** from multiple generations
- **Responsive design** works on mobile & desktop
- **Clean UI** with Pokémon-themed styling

## 🛠 Built With

- ![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-yellow)
- ![PokeAPI](https://img.shields.io/badge/PokeAPI-v2-red)
- ![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5)
- ![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3)

## 🚀 Getting Started

1. Clone the repo:
```bash
git clone https://github.com/Munique-Feitoza/pokedex_in_js.git
```
2. Open **index.html** in your browser
3. Search for your favorite Pokémon!

## 💻 Code Highlights
Fetching Pokémon Data
```
async function getPokemonData(nameOrId) {
  try {
    const response = await fetch(`https://pokeapi.co/api/v2/pokemon/${nameOrId}`);
    return await response.json();
  } catch (error) {
    console.error("Error fetching Pokémon:", error);
  }
}
```

## Displaying Pokémon Info
```
function displayPokemon(pokemon) {
  document.getElementById('pokemon-name').textContent = 
    `#${pokemon.id} ${pokemon.name.charAt(0).toUpperCase() + pokemon.name.slice(1)}`;
  
  document.getElementById('pokemon-image').src = 
    pokemon.sprites.versions['generation-v']['black-white'].animated.front_default;
}
```

## 🌟 Upcoming Features

Evolution chains
Comparison tool
Favorite Pokémon storage
Advanced search filters
Dark/Light mode toggle

## 👩💻 About the Developer
Munique Feitoza
GitHub: [Munique-Feitoza](https://github.com/Munique-Feitoza)
LinkedIn: [Munique Feitoza](https://linkedin.com/in/munique-feitoza-77034b231/)

"Built with passion for Pokémon fans everywhere!"
