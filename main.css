<html><head><base href="https://www.resource-empire.com/"><title>Resource Empire: Defeat the Mighty Boss!</title>
<style>
body, html {
    margin: 0;
    padding: 0;
    height: 100%;
    font-family: 'Arial', sans-serif;
    background: linear-gradient(45deg, #2c3e50, #3498db);
    color: #ecf0f1;
}
.game-container {
    display: flex;
    height: 100vh;
}
.sidebar {
    width: 250px; 
    background: rgba(0,0,0,0.5);
    padding: 15px; 
    overflow-y: auto;
}
.main-area {
    display: flex;
    flex-wrap: wrap;
    flex-grow: 1;
    padding: 15px; 
    overflow-y: auto;
}
h1 {
    font-size: 1.5em; 
}
h2 {
    font-size: 1.2em; 
    margin-top: 10px; 
}
.resource, .unit, .defense-value, .strength-value {
    margin-bottom: 5px; 
    padding: 5px; 
    background: rgba(255,255,255,0.1);
    border-radius: 5px;
}
.building, .recruit-btn, #boss-button, .research-btn {
    position: relative;
    padding-bottom: 20px; 
    display: inline-block;
    width: 90px; 
    height: 120px; 
    margin: 5px; 
    background: rgba(255,255,255,0.2);
    border-radius: 10px;
    text-align: center;
    cursor: pointer;
    transition: transform 0.3s ease;
}
.cost {
    position: absolute;
    bottom: 5px;
    left: 5px;
    right: 5px;
    background: rgba(0,0,0,0.7);
    color: white;
    font-size: 0.7em; 
    padding: 2px;
    border-radius: 3px;
}
.building svg, .recruit-btn svg {
    width: 60px; 
    height: 60px; 
    margin-bottom: 0; 
    margin-top: 5px; 
}
.building:hover, .recruit-btn:hover, #boss-button:hover, .research-btn:hover {
    transform: scale(1.05);
}
#notification-area {
    position: fixed;
    top: 10px;
    right: 10px;
    width: 300px;
}
.notification {
    background: rgba(0,0,0,0.7);
    color: #fff;
    padding: 10px;
    margin-bottom: 10px;
    border-radius: 5px;
    animation: fadeIn 0.5s, fadeOut 0.5s 2.5s forwards;
}
@keyframes fadeIn {
    from { opacity: 0; }
    to { opacity: 1; }
}
@keyframes fadeOut {
    from { opacity: 1; }
    to { opacity: 0; }
}
#boss-button {
    background: linear-gradient(45deg, #c0392b, #e74c3c);
    color: white;
    font-weight: bold;
    font-size: 1em; 
    width: 170px; 
    height: 60px; 
    line-height: 60px; 
    margin-top: 20px;
}
#boss-health-bar {
    width: 100%;
    height: 15px; 
    background-color: #e74c3c;
    margin-top: 10px;
    position: relative;
}
#boss-health {
    width: 100%;
    height: 100%;
    background-color: #2ecc71;
    transition: width 0.3s ease;
}
#boss-health-text {
    position: absolute;
    width: 100%;
    text-align: center;
    line-height: 15px; 
    color: white;
    font-weight: bold;
}
#timer {
    font-size: 1.2em;
    margin-bottom: 10px;
    color: #f39c12;
}
#defense-page {
    display: none;
    padding: 20px;
    background: rgba(0,0,0,0.7);
    border-radius: 10px;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    z-index: 1000;
}
#back-to-main {
    margin-top: 20px;
    padding: 10px;
    background: #3498db;
    border: none;
    color: white;
    cursor: pointer;
    border-radius: 5px;
}
#boss-info {
    margin-top: 20px;
    padding: 10px;
    background: rgba(255,255,255,0.1);
    border-radius: 5px;
}
#start-reset-game {
    display: block;
    width: 100%;
    padding: 10px;
    margin-bottom: 10px;
    background-color: #2ecc71;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-weight: bold;
}
#start-reset-game:hover {
    background-color: #27ae60;
}
#boss-stats {
    margin-bottom: 10px; 
    padding: 5px; 
    background: rgba(255,255,255,0.1);
    border-radius: 5px;
}
#boss-stats div {
    margin-bottom: 5px;
}
#hero-stats, #neutral-armies {
    margin-bottom: 10px; 
    padding: 5px; 
    background: rgba(255,255,255,0.1);
    border-radius: 5px;
}
.hero-stat, .neutral-army {
    margin-bottom: 5px;
}
.battle-btn {
    padding: 5px 10px;
    background: #3498db;
    color: white;
    border: none;
    border-radius: 3px;
    cursor: pointer;
}
.battle-btn:hover {
    background: #2980b9;
}
.research-btn {
    display: inline-block;
    width: 170px; 
    height: 60px; 
    margin: 10px;
    background: rgba(255,255,255,0.2);
    border-radius: 10px;
    text-align: center;
    cursor: pointer;
    transition: transform 0.3s ease;
}
.research-btn:hover {
    transform: scale(1.05);
}
#specialization-choice {
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    background: rgba(0,0,0,0.8);
    padding: 20px;
    border-radius: 10px;
    z-index: 1000;
    color: white;
    text-align: center;
}
#specialization-choice button {
    display: block;
    width: 100%;
    padding: 10px;
    margin: 10px 0;
    background-color: #3498db;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
}
#specialization-choice button:hover {
    background-color: #2980b9;
}
.left-column, .right-column {
    flex: 1;
    min-width: 320px; 
    padding: 0 5px;
}
#buildings, #recruitment, #research-options {
    display: flex;
    flex-wrap: wrap;
    justify-content: flex-start;
}
#empire-army-viz {
    width: 200px;
    height: 200px;
    background-color: rgba(255, 255, 255, 0.1);
    margin-bottom: 10px;
    position: relative;
}
#city-viz {
    margin-top: 20px;
    height: 80px; 
}
.building svg {
    width: 60px; 
    height: 60px; 
    margin-bottom: 0;
    margin-top: 5px;
}
.recruit-btn svg {
    width: 60px; 
    height: 60px; 
    margin-bottom: 0;
    margin-top: 5px;
}
#population-viz {
    margin-bottom: 20px;
}
#population-bar {
    width: 100%;
    height: 20px;
    background-color: #e0e0e0;
    border-radius: 10px;
    overflow: hidden;
}
#population-progress {
    height: 100%;
    background-color: #4CAF50;
    width: 0%;
    transition: width 0.5s ease-in-out;
}
#population-text {
    text-align: center;
    margin-top: 5px;
    font-weight: bold;
}
#game-over-box {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.7);
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 1000;
}
.message-box {
    background-color: #fff;
    padding: 20px;
    border-radius: 10px;
    text-align: center;
}
#try-again-btn {
    margin-top: 20px;
    padding: 10px 20px;
    background-color: #3498db;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
}
#try-again-btn:hover {
    background-color: #2980b9;
}
#victory-box {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.7);
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 1000;
}
#victory-box .message-box {
    background-color: #fff;
    padding: 20px;
    border-radius: 10px;
    text-align: center;
    color: #333;
}
#restart-btn {
    margin-top: 20px;
    padding: 10px 20px;
    background-color: #2ecc71;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
}
#restart-btn:hover {
    background-color: #27ae60;
}
.tooltip {
    display: none;
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    background-color: rgba(0, 0, 0, 0.8);
    color: white;
    padding: 10px;
    border-radius: 5px;
    z-index: 1000;
    text-align: left;
}
#leaderboard-container {
    background-color: rgba(0, 0, 0, 0.8);
    padding: 20px;
    border-radius: 10px;
    color: white;
    margin-top: 20px;
}
#leaderboard {
    width: 100%;
    border-collapse: collapse;
}
#leaderboard th, #leaderboard td {
    padding: 10px;
    text-align: left;
    border-bottom: 1px solid #ddd;
}
#leaderboard-form {
    margin-top: 20px;
    margin-bottom: 20px;
}
#player-name {
    padding: 5px;
    margin-right: 10px;
}
#boss-attack-timer {
    font-size: 1.2em;
    margin-bottom: 15px;
    padding: 10px;
    background-color: rgba(255, 0, 0, 0.1);
    border-radius: 5px;
    text-align: center;
}
</style>
</head>
<body>
<div class="game-container">
    <div class="sidebar">
        <h1>Resource Empire</h1>
        <button id="start-reset-game">Start/Reset Game</button>
        <div id="timer">Time: 00:00:00</div>
        <div id="resources">
            <!-- Resources will be dynamically added here -->
        </div>
        <h2>Population</h2>
        <div id="population"></div>
        <h2>Army</h2>
        <div id="army">
            <!-- Army units will be dynamically added here -->
        </div>
    </div>
    <div class="main-area">
        <div class="left-column">
            <div id="intro-text" style="margin-bottom: 15px; padding: 10px; background-color: rgba(255,255,255,0.1); border-radius: 5px;">
                Welcome to Heroes Campaign!
                <ul style="margin-top: 10px; padding-left: 20px;">
                    <li>Build your empire and recruit armies.</li>
                    <li>Try to survive the Dragon Emperor who seeks to annihilate you!</li>
                    <li>University unlocks research.</li>
                    <li>Fighting neutral armies gains experience for the Hero and iron.</li>
                    <li>Archers and Ballistas are in cover and cant be killed.</li>
                    <li>Troubadours don't fight but buff the army and give experience.</li>
                </ul>
            </div>
            <h2>Buildings</h2>
            <div id="buildings">
                <!-- Buildings will be dynamically added here -->
            </div>
            <h2>Recruitment</h2>
            <div id="recruitment">
                <!-- Recruitment buttons will be dynamically added here -->
            </div>
            <h2>Research</h2>
            <div id="research-options" style="display: none;">
                <!-- Research options will be dynamically added here -->
            </div>
        </div>
        <div class="right-column">
            <h2>Dragon Emperor Attack Timer</h2>
            <div id="boss-attack-timer">Next attack in: 01:00</div>
            <h2>Empire Army Visualization</h2>
            <div id="empire-army-viz"></div>
            <h2>Population Visualization</h2>
            <div id="population-viz">
                <div id="population-bar">
                    <div id="population-progress"></div>
                </div>
                <div id="population-text"></div>
            </div>
            <h2>City Visualization</h2>
            <div id="city-viz"></div>
            <h2>Empire Defense and Strength</h2>
            <div id="empire-defense"></div>
            <div id="empire-strength"></div>
            <h2>Dragon Emperor Stats</h2>
            <div id="boss-stats">
                <div id="boss-health-stat"></div>
                <div id="boss-strength-stat"></div>
            </div>
            <h2>Empire Hero</h2>
            <div id="hero-stats"></div>
            <h2>Neutral Armies</h2>
            <div id="neutral-armies"></div>
            <h2>Dragon Emperor Battle</h2>
            <div id="boss-battle">
                <div id="boss-button">Fight the Dragon!</div>
                <div id="boss-health-bar">
                    <div id="boss-health"></div>
                    <div id="boss-health-text">100%</div>
                </div>
            </div>
        </div>
    </div>
</div>
<div id="damage-tooltip" class="tooltip"></div>
<div id="notification-area"></div>
<div id="defense-page">
    <h2>Empire Defense and Strength</h2>
    <div id="empire-stats"></div>
    <div id="boss-info">
        <h3>Dragon Emperor Information</h3>
        <div id="boss-strength"></div>
        <div id="boss-attack-timer"></div>
    </div>
    <button id="back-to-main">Back to Main Page</button>
</div>
<div id="game-over-box" style="display: none;">
    <div class="message-box">
        <h2>Game Over</h2>
        <p>Game is lost, better luck next time</p>
        <button id="try-again-btn">Try Again</button>
    </div>
</div>
<div id="victory-box" style="display: none;">
    <div class="message-box">
        <h2>Congratulations!</h2>
        <p>You've defeated the Dragon Emperor and won the game!</p>
        <p id="victory-time"></p>
        <form id="leaderboard-form">
            <input type="text" id="player-name" placeholder="Enter your name" required>
            <button type="submit">Submit to Leaderboard</button>
        </form>
        <button id="restart-btn">Play Again</button>
    </div>
</div>
<div id="leaderboard-container" style="display: none;">
    <h2>Leaderboard</h2>
    <table id="leaderboard">
        <thead>
            <tr>
                <th>Rank</th>
                <th>Name</th>
                <th>Time</th>
            </tr>
        </thead>
        <tbody>
            <!-- Leaderboard entries will be inserted here -->
        </tbody>
    </table>
</div>
<div id="specialization-choice" style="display: none;">
    <h2>Choose a Specialization</h2>
    <button onclick="chooseSpecialization('gatherer')">Gatherer</button>
    <button onclick="chooseSpecialization('healer')">Healer</button>
    <button onclick="chooseSpecialization('fighter')">Fighter</button>
</div>
<script>
const resources = {
    gold: { name: "Gold", amount: 500, perSecond: 2, initialAmount: 500 },
    wood: { name: "Wood", amount: 800, perSecond: 1, initialAmount: 800 },
    food: { name: "Food", amount: 200, perSecond: 1, initialAmount: 200 },
    iron: { name: "Iron", amount: 100, perSecond: 0, initialAmount: 100 }
};

const buildings = {
    mine: { name: "Gold Mine", cost: { wood: 100 }, produces: { gold: 2} },
    lumbermill: { name: "Lumber Mill", cost: { wood: 50 }, produces: { wood: 2 } },
    farm: { name: "Farm", cost: { wood: 100}, produces: { food: 2 } },
    ironmine: { name: "Iron Mine", cost: { gold: 100, wood: 100 }, produces: { iron: 1 } },
    university: { name: "University", cost: { gold: 500, wood: 200, iron: 50 }, produces: {} }
};

const buildingCounts = {
    mine: 0,
    lumbermill: 0,
    farm: 0,
    ironmine: 0,
    university: 0
};

const research = {
    unitUpgrade: { name: "Unit Upgrade", cost: { iron: 400 }, effect: { strength: 1, defense: 1 }, level: 0, maxLevel: 5 },
    populationGrowth: { name: "Population Growth", cost: { food: 1000 }, effect: { growth: 1 }, level: 0, maxLevel: 5 },
    ironMineUnlock: { name: "Iron Mining Technology", cost: { gold: 500, wood: 500 }, effect: { unlockIronMine: true }, level: 0, maxLevel: 1 },
    ballistaUnlock: { name: "Ballista Unlock", cost: { gold: 500, iron: 200 }, effect: { unlockBallista: true }, level: 0, maxLevel: 1 },
    musicAcademy: { name: "Music Academy", cost: { gold: 200, wood: 200 }, effect: { unlockTroubadour: true }, level: 0, maxLevel: 1 }
};

let hasUniversity = false;
let populationGrowthRate = 0; 
let wallDefenseMultiplier = 1;
let siegeEngineUnlocked = false;
let ironMineUnlocked = false;
let bossAttackCount = 0; 
let maxPopulationReached = 1000; 

const units = {
    soldier: { name: "Soldier", cost: { food: 50, gold: 30 }, strength: 3, defense: 8, upgradeBonus: { strength: 1, defense: 1 } },
    archer: { name: "Archer", cost: { food: 70, wood: 30 }, strength: 7, defense: 0, upgradeBonus: { strength: 2, defense: 0.5 } },
    knight: { name: "Knight", cost: { food: 150, iron: 100 }, strength: 20, defense: 50, upgradeBonus: { strength: 2, defense: 2 } },
    ballista: { name: "Ballista", cost: { gold: 200, wood: 100, iron: 100 }, strength: 50, defense: 5, upgradeBonus: { strength: 4, defense: 1 } },
    troubadour: { name: "Troubadour", cost: { gold: 80, food: 80 }, strength: 0, defense: 1, upgradeBonus: { strength: 0, defense: 0.5 } }
};

const army = {
    soldier: 0,
    archer: 0,
    knight: 0,
    ballista: 0,
    troubadour: 0
};

let population = 1000; 
let bossHealth = 10000;
const bossMaxHealth = 10000;
let gameTime = 0;
let lastBossAttackTime = 0;
let bossAttackTimer = 60; 

const hero = {
    name: "Empire Hero",
    strength: 10,
    experience: 0,
    level: 1,
    specializations: {
        gatherer: 0,
        healer: 0,
        fighter: 0
    }
};

const neutralArmies = [
    { name: "Bandit Camp", strength: 50, rewards: { iron: 50, experience: 20 } },
    { name: "Rogue Knights", strength: 100, rewards: { iron: 100, experience: 40 } },
    { name: "Ancient Ruins Guardians", strength: 200, rewards: { gold: 300, iron: 200, experience: 80 } }
];

function calculateTotalDefense() {
    return Object.keys(army).reduce((sum, unit) => {
        return sum + army[unit] * units[unit].defense;
    }, 0);
}

function calculateTotalArmyStrength() {
    let totalStrength = Object.keys(army).reduce((sum, unit) => {
        return sum + army[unit] * units[unit].strength;
    }, 0) + hero.strength;

    // Apply Troubadour buff
    if (army.troubadour > 0) {
        totalStrength += (army.soldier + army.archer + army.knight + army.ballista) * army.troubadour;
    }

    return totalStrength;
}

function updateResources() {
    const resourcesContainer = document.getElementById('resources');
    resourcesContainer.innerHTML = '';
    Object.keys(resources).forEach(key => {
        const resource = resources[key];
        const resourceElement = document.createElement('div');
        resourceElement.className = 'resource';
        resourceElement.innerHTML = `
            <strong>${resource.name}:</strong> ${Math.floor(resource.amount)}
            <small>(+${resource.perSecond}/s)</small>
        `;
        resourcesContainer.appendChild(resourceElement);
    });
}

function updatePopulation() {
    const populationElement = document.getElementById('population');
    populationElement.innerHTML = `
        <div class="resource">
            <strong>Population:</strong> ${Math.floor(population).toLocaleString()}
            <small>(+${populationGrowthRate}/s)</small>
        </div>
    `;
    updatePopulationVisualization(); 
}

function updatePopulationVisualization() {
    maxPopulationReached = Math.max(maxPopulationReached, population);
    
    const progressBar = document.getElementById('population-progress');
    const populationText = document.getElementById('population-text');
    
    const percentage = Math.min((population / maxPopulationReached) * 100, 100);
    progressBar.style.width = `${percentage}%`;
    populationText.textContent = `Population: ${Math.floor(population).toLocaleString()} / ${maxPopulationReached.toLocaleString()}`;
}

function updateArmy() {
    const armyContainer = document.getElementById('army');
    armyContainer.innerHTML = '';
    Object.keys(army).forEach(key => {
        const unit = units[key];
        const unitElement = document.createElement('div');
        unitElement.className = 'unit';
        unitElement.innerHTML = `
            <strong>${unit.name}:</strong> ${army[key]}
            <small>(Strength: ${unit.strength}, Defense: ${unit.defense})</small>
        `;
        armyContainer.appendChild(unitElement);
    });
    updateEmpireArmyVisualization(); 
}

function createBuildings() {
    const buildingsContainer = document.getElementById('buildings');
    buildingsContainer.innerHTML = ''; 
    Object.keys(buildings).forEach(key => {
        if (key === 'ironmine' && !ironMineUnlocked) return; 
        const building = buildings[key];
        const buildingElement = document.createElement('div');
        buildingElement.className = 'building';
        buildingElement.innerHTML = `
            ${getBuildingIcon(key)}
            <div>${building.name}</div>
            <div class="cost">${formatCost(building.cost)}</div>
        `;
        buildingElement.onclick = () => buyBuilding(key);
        buildingsContainer.appendChild(buildingElement);
    });
}

function getBuildingIcon(building) {
    const icons = {
        mine: '<svg viewBox="0 0 24 24" width="60" height="60"><path fill="#FFD700" d="M12 2L2 7l10 5 10-5-10-5zM2 17l10 5 10-5-10-5-10 5zm0-5l10 5 10-5-10-5-10 5z"/></svg>',
        lumbermill: '<svg viewBox="0 0 24 24" width="60" height="60"><path fill="#8B4513" d="M17 3H7c-1.1 0-2 .9-2 2v16l7-3 7 3V5c0-1.1-.9-2-2-2zm-5 9.5L8.5 15l2-5.5L12 7l1.5 2.5 2 5.5L12 12.5z"/></svg>',
        farm: '<svg viewBox="0 0 24 24" width="60" height="60"><path fill="#32CD32" d="M15 4v2h3v2h-3v2h3v2h-3v8h-2v-8H6v8H4v-2H1v-2h3v-2H1v-2h3V6H1V4h3V2h2v2h8V2h2v2h3v2h-2v2h2v2h-2v2h-2v-2H7v2H5v-2H1v-2h2v-2H1v-2h3V6H1V4h3V2H5z"/></svg>',
        ironmine: '<svg viewBox="0 0 24 24" width="60" height="60"><path fill="#708090" d="M12 2L2 7l10 5 10-5-10-5zM2 17l10 5 10-5-10-5-10 5zm0-5l10 5 10-5-10-5-10 5zm10-5l-10 5 10 5 10-5-10-5z"/></svg>',
        university: '<svg viewBox="0 0 24 24" width="60" height="60"><path fill="#4169E1" d="M12 3L1 9l11 6 9-4.91V17h2V9L12 3zm0 14.53l-8-4.36v1.75l8 4.38 8-4.38V13.3L12 17.53z"/></svg>'
    };
    return icons[building] || '';
}

const unitIcons = {
    soldier: '<svg viewBox="0 0 50 50" width="60" height="60"><path fill="#4682B4" d="M25,2 C18,2 13,7 13,13 C13,17 15,20 18,22 L18,28 L12,42 L38,42 L32,28 L32,22 C35,20 37,17 37,13 C37,7 32,2 25,2 zM25,44 L20,48 L30,48 Z"/></svg>',
    archer: '<svg viewBox="0 0 50 50" width="60" height="60"><path fill="#228B22" d="M10,25 L40,25 M25,10 L25,40 M15,15 L35,35 M35,15 L15,35"/><circle cx="25" cy="25" r="20" fill="none" stroke="#228B22" stroke-width="2"/></svg>',
    knight: '<svg viewBox="0 0 50 50" width="60" height="60"><path fill="#8B4513" d="M25,2 C18,2 13,7 13,13 C13,17 15,20 18,22 L18,28 L12,42 L38,42 L32,28 L32,22 C35,20 37,17 37,13 C37,7 32,2 25,2 zM25,44 L20,48 L30,48 Z"/></svg>',
    ballista: '<svg viewBox="0 0 50 50" width="60" height="60"><path fill="#8B4513" d="M10,40 L40,40 L25,10 Z M23,38 L27,38 L25,20 Z"/></svg>',
    troubadour: '<svg viewBox="0 0 50 50" width="60" height="60"><circle cx="25" cy="25" r="20" fill="#FF6347"/><text x="25" y="30" text-anchor="middle" font-size="16" fill="#ffffff">T</text></svg>'
};

function createRecruitmentButtons() {
    const recruitmentContainer = document.getElementById('recruitment');
    recruitmentContainer.innerHTML = ''; 
    Object.keys(units).forEach(key => {
        if (key === 'ballista' && research.ballistaUnlock.level === 0) return;
        if (key === 'troubadour' && research.musicAcademy.level === 0) return;
        const unit = units[key];
        const buttonElement = document.createElement('div');
        buttonElement.className = 'recruit-btn';
        buttonElement.innerHTML = `
            ${unitIcons[key]}
            <div>${unit.name}</div>
            <div class="cost">${formatCost(unit.cost)}</div>
        `;
        buttonElement.onclick = () => recruitUnit(key);
        
        // Add tooltip for troubadour
        if (key === 'troubadour') {
            buttonElement.title = "Buff the army and give passive experience to the Hero";
        }
        
        recruitmentContainer.appendChild(buttonElement);
    });
}

function createResearchOptions() {
    const researchContainer = document.getElementById('research-options');
    researchContainer.innerHTML = '';
    Object.keys(research).forEach(key => {
        const option = research[key];
        if (option.level < option.maxLevel) {
            const buttonElement = document.createElement('div');
            buttonElement.className = 'research-btn';
            buttonElement.innerHTML = `
                <div>${option.name} (Level ${option.level}/${option.maxLevel})</div>
                <div class="cost">${formatCost(option.cost)}</div>
            `;
            buttonElement.onclick = () => performResearch(key);
            researchContainer.appendChild(buttonElement);
        }
    });
}

function performResearch(researchKey) {
    const option = research[researchKey];
    if (option.level < option.maxLevel && canAfford(option.cost)) {
        Object.keys(option.cost).forEach(resource => {
            resources[resource].amount -= option.cost[resource];
        });
        option.level++;
        applyResearchEffects(researchKey);
        updateResources();
        createResearchOptions();
        createRecruitmentButtons(); 
        notify(`${option.name} researched to level ${option.level}!`);
    } else if (option.level >= option.maxLevel) {
        notify("Research already at maximum level!", "error");
    } else {
        notify("Not enough resources for research!", "error");
    }
}

function applyResearchEffects(researchKey) {
    const option = research[researchKey];
    if (researchKey === 'unitUpgrade') {
        Object.keys(units).forEach(unit => {
            units[unit].strength += option.effect.strength;
            units[unit].defense += option.effect.defense;
        });
        updateArmy();
    } else if (researchKey === 'populationGrowth') {
        populationGrowthRate += option.level * option.effect.growth;
    } else if (researchKey === 'ironMineUnlock') {
        ironMineUnlocked = true;
        notify("Iron Mine has been unlocked!", "success");
        createBuildings(); 
    } else if (researchKey === 'ballistaUnlock') {
        notify("Ballista has been unlocked!", "success");
        createRecruitmentButtons();
    } else if (researchKey === 'musicAcademy') {
        notify("Troubadour has been unlocked!", "success");
        createRecruitmentButtons();
    }
}

function createNeutralArmyButtons() {
    const neutralArmiesContainer = document.getElementById('neutral-armies');
    neutralArmiesContainer.innerHTML = '';
    neutralArmies.forEach((army, index) => {
        const armyElement = document.createElement('div');
        armyElement.className = 'neutral-army';
        armyElement.innerHTML = `
            <strong>${army.name}</strong> (Strength: ${army.strength})
            <button class="battle-btn" onclick="battleNeutralArmy(${index})">Battle</button>
        `;
        neutralArmiesContainer.appendChild(armyElement);
    });
}

function buyBuilding(buildingKey) {
    const building = buildings[buildingKey];
    if (buildingKey === 'ironmine' && !ironMineUnlocked) {
        notify("Iron Mine is not yet unlocked!", "error");
        return;
    }
    if (canAfford(building.cost)) {
        if (buildingKey === 'university' && buildingCounts['university'] >= 1) {
            notify("You can only build one university!", "error");
            return;
        }
        Object.keys(building.cost).forEach(resource => {
            resources[resource].amount -= building.cost[resource];
        });
        if (buildingKey === 'university') {
            hasUniversity = true;
            document.getElementById('research-options').style.display = 'block';
            createResearchOptions();
        } else {
            Object.keys(building.produces).forEach(resource => {
                resources[resource].perSecond += building.produces[resource];
            });
        }
        buildingCounts[buildingKey]++;
        updateResources();
        updateCityVisualization(); 
        notify(`${building.name} purchased!`);
    } else {
        notify("Not enough resources!", "error");
    }
}

function updateCityVisualization() {
    const cityVizContainer = document.getElementById('city-viz');
    cityVizContainer.innerHTML = '<h3>City Visualization</h3>';

    const svg = document.createElementNS("http://www.w3.org/2000/svg", "svg");
    svg.setAttribute("width", "100%");
    svg.setAttribute("height", "80"); 

    let x = 0;
    const y = 40; 
    const buildingWidth = 20;
    const buildingSpacing = 5;

    Object.entries(buildingCounts).forEach(([building, count]) => {
        for (let i = 0; i < count; i++) {
            const foreignObject = document.createElementNS("http://www.w3.org/2000/svg", "foreignObject");
            foreignObject.setAttribute("x", x);
            foreignObject.setAttribute("y", y - 10);
            foreignObject.setAttribute("width", buildingWidth);
            foreignObject.setAttribute("height", buildingWidth);
            
            const iconDiv = document.createElement("div");
            iconDiv.innerHTML = getBuildingIcon(building);
            iconDiv.firstChild.setAttribute("width", buildingWidth);
            iconDiv.firstChild.setAttribute("height", buildingWidth);
            
            foreignObject.appendChild(iconDiv);
            svg.appendChild(foreignObject);

            x += buildingWidth + buildingSpacing;
        }
    });

    cityVizContainer.appendChild(svg);
}

function updateWallDefense() {
    const empireDefenseElement = document.getElementById('empire-defense');
    empireDefenseElement.innerHTML = `
        <div class="defense-value">
            <strong>Total Empire Defense:</strong> ${calculateTotalDefense()}
        </div>
    `;
}

function recruitUnit(unitKey) {
    const unit = units[unitKey];
    if (unitKey === 'ballista' && research.ballistaUnlock.level === 0) {
        notify("Ballista is not yet unlocked!", "error");
        return;
    }
    if (unitKey === 'troubadour' && research.musicAcademy.level === 0) {
        notify("Troubadour is not yet unlocked!", "error");
        return;
    }
    if (canAfford(unit.cost)) {
        Object.keys(unit.cost).forEach(resource => {
            resources[resource].amount -= unit.cost[resource];
        });
        army[unitKey]++;
        updateResources();
        updateArmy();
        updateEmpireArmyVisualization(); 
        notify(`${unit.name} recruited!`);
    } else {
        notify("Not enough resources to recruit!", "error");
    }
}

function battleNeutralArmy(armyIndex) {
    const neutralArmy = neutralArmies[armyIndex];
    const totalStrength = hero.strength + calculateTotalArmyStrength();
    const battleReport = {
        enemyName: neutralArmy.name,
        enemyStrength: neutralArmy.strength,
        empireStrength: totalStrength,
        soldiersLost: 0,
        knightsLost: 0,
        troubadoursLost: 0,
        populationLost: 0,
        result: ''
    };
    
    if (totalStrength > neutralArmy.strength) {
        Object.keys(neutralArmy.rewards).forEach(reward => {
            if (reward === 'experience') {
                hero.experience += neutralArmy.rewards[reward];
                checkHeroLevelUp();
            } else {
                resources[reward].amount += neutralArmy.rewards[reward];
            }
        });
        
        const armyDamage = Math.floor(neutralArmy.strength * 0.5);
        distributeNeutralArmyDamage(armyDamage, battleReport);
        
        battleReport.result = 'Victory';
        notify(`Victory against ${neutralArmy.name}! Gained rewards and experience.`, "success");
    } else {
        const armyDamage = Math.floor(neutralArmy.strength * 0.8);
        distributeNeutralArmyDamage(armyDamage, battleReport);
        
        battleReport.result = 'Defeat';
        notify(`Defeated by ${neutralArmy.name}.`, "error");
    }
    
    updateHeroStats();
    updateResources();
    updatePopulation();
    updateArmy();
    
    showNeutralArmyBattleReport(battleReport);
    
    if (population <= 0) {
        gameOver();
    }
}

function distributeNeutralArmyDamage(totalDamage, battleReport) {
    let remainingDamage = totalDamage;
    
    // Damage to soldiers
    if (army.soldier > 0 && remainingDamage > 0) {
        const soldierDefense = units.soldier.defense;
        const soldiersLost = Math.min(army.soldier, Math.floor(remainingDamage / soldierDefense));
        army.soldier -= soldiersLost;
        remainingDamage -= soldiersLost * soldierDefense;
        battleReport.soldiersLost = soldiersLost;
    }
    
    // Damage to knights 
    if (army.knight > 0 && remainingDamage > 0) {
        const knightDefense = units.knight.defense;
        const knightsLost = Math.min(army.knight, Math.floor(remainingDamage / knightDefense));
        army.knight -= knightsLost;
        remainingDamage -= knightsLost * knightDefense;
        battleReport.knightsLost = knightsLost;
    }

    // Damage to troubadours
    if (army.troubadour > 0 && remainingDamage > 0) {
        const troubadourDefense = units.troubadour.defense;
        const troubadoursLost = Math.min(army.troubadour, Math.floor(remainingDamage / troubadourDefense));
        army.troubadour -= troubadoursLost;
        remainingDamage -= troubadoursLost * troubadourDefense;
        battleReport.troubadoursLost = troubadoursLost;
    }
    
    // Damage to population
    if (remainingDamage > 0) {
        const populationLost = Math.min(population, remainingDamage);
        population = Math.max(0, population - populationLost);
        battleReport.populationLost = populationLost;
    }
    
    updateEmpireArmyVisualization();
}

function showNeutralArmyBattleReport(battleReport) {
    const tooltipContent = `
        <strong>Battle Report: ${battleReport.enemyName}</strong><br>
        Result: ${battleReport.result}<br>
        Enemy Strength: ${battleReport.enemyStrength}<br>
        Empire Strength: ${battleReport.empireStrength}<br>
        Soldiers Lost: ${battleReport.soldiersLost}<br>
        Knights Lost: ${battleReport.knightsLost}<br>
        Troubadours Lost: ${battleReport.troubadoursLost}<br>
        Population Lost: ${battleReport.populationLost}
    `;
    
    const tooltip = document.getElementById('damage-tooltip');
    tooltip.innerHTML = tooltipContent;
    tooltip.style.display = 'block';
    
    setTimeout(() => {
        tooltip.style.display = 'none';
    }, 5000); // Hide tooltip after 5 seconds
}

function gameOver() {
    document.getElementById('game-over-box').style.display = 'flex';
}

function checkHeroLevelUp() {
    const experienceNeeded = hero.level * 100;
    if (hero.experience >= experienceNeeded) {
        hero.experience -= experienceNeeded;
        heroLevelUp();
    }
}

function heroLevelUp() {
    hero.level++;
    hero.strength += 5;
    showSpecializationChoice();
}

function showSpecializationChoice() {
    document.getElementById('specialization-choice').style.display = 'block';
}

function chooseSpecialization(specialization) {
    hero.specializations[specialization]++;
    applySpecializationEffects(specialization);
    document.getElementById('specialization-choice').style.display = 'none';
    updateHeroStats();
    notify(`Specialization in ${specialization} increased!`, "success");
}

function applySpecializationEffects(specialization) {
    switch (specialization) {
        case 'gatherer':
            Object.keys(resources).forEach(key => {
                resources[key].perSecond += 1;
            });
            break;
        case 'healer':
            populationGrowthRate += 1;
            break;
        case 'fighter':
            hero.strength += 10;
            break;
    }
}

function updateHeroStats() {
    const heroStatsElement = document.getElementById('hero-stats');
    heroStatsElement.innerHTML = `
        <div class="hero-stat"><strong>Hero Level:</strong> ${hero.level}</div>
        <div class="hero-stat"><strong>Hero Strength:</strong> ${hero.strength}</div>
        <div class="hero-stat"><strong>Hero Experience:</strong> ${hero.experience}/${hero.level * 100}</div>
        <div class="hero-stat"><strong>Experience Gain:</strong> ${army.troubadour}/s</div>
        <div class="hero-stat"><strong>Specializations:</strong></div>
        <div class="hero-stat">Gatherer: ${hero.specializations.gatherer}</div>
        <div class="hero-stat">Healer: ${hero.specializations.healer}</div>
        <div class="hero-stat">Fighter: ${hero.specializations.fighter}</div>
    `;
}

function canAfford(cost) {
    return Object.keys(cost).every(resource => resources[resource].amount >= cost[resource]);
}

function notify(message, type = "success") {
    const notificationArea = document.getElementById('notification-area');
    const notification = document.createElement('div');
    notification.className = `notification ${type}`;
    notification.textContent = message;
    notificationArea.appendChild(notification);
    setTimeout(() => {
        notificationArea.removeChild(notification);
    }, 3000);
}

function updateTimer() {
    const hours = Math.floor(gameTime / 3600);
    const minutes = Math.floor((gameTime % 3600) / 60);
    const seconds = gameTime % 60;
    document.getElementById('timer').textContent = `Time: ${String(hours).padStart(2, '0')}:${String(minutes).padStart(2, '0')}:${String(seconds).padStart(2, '0')}`;
}

function formatCost(cost) {
    return Object.entries(cost).map(([resource, amount]) => `${amount} ${resource}`).join(', ');
}

function showVictoryMessage() {
    const victoryBox = document.getElementById('victory-box');
    const victoryTime = document.getElementById('victory-time');
    const hours = Math.floor(gameTime / 3600);
    const minutes = Math.floor((gameTime % 3600) / 60);
    const seconds = gameTime % 60;
    const timeString = `${String(hours).padStart(2, '0')}:${String(minutes).padStart(2, '0')}:${String(seconds).padStart(2, '0')}`;
    
    victoryTime.textContent = `You beat the game in ${timeString}!`;
    victoryBox.style.display = 'flex';
    
    document.getElementById("leaderboard-form").onsubmit = function(e) {
        e.preventDefault();
        const playerName = document.getElementById("player-name").value;
        submitToLeaderboard(playerName, timeString);
    };
}

function submitToLeaderboard(playerName, time) {
    // This is a mock function. In a real implementation, you would send this data to a server.
    console.log(`Submitting to leaderboard: ${playerName} - ${time}`);
    
    // Mock leaderboard data
    const leaderboardData = [
        { name: playerName, time: time },
        { name: "Alice", time: "01:30:00" },
        { name: "Bob", time: "01:45:30" },
        { name: "Charlie", time: "02:00:15" },
        { name: "David", time: "02:15:45" }
    ];
    
    // Sort leaderboard data
    leaderboardData.sort((a, b) => {
        const timeA = a.time.split(':').reduce((acc, time) => (60 * acc) + +time);
        const timeB = b.time.split(':').reduce((acc, time) => (60 * acc) + +time);
        return timeA - timeB;
    });
    
    displayLeaderboard(leaderboardData);
}

function displayLeaderboard(leaderboardData) {
    const leaderboardBody = document.querySelector("#leaderboard tbody");
    leaderboardBody.innerHTML = "";
    
    leaderboardData.forEach((entry, index) => {
        const row = document.createElement("tr");
        row.innerHTML = `
            <td>${index + 1}</td>
            <td>${entry.name}</td>
            <td>${entry.time}</td>
        `;
        leaderboardBody.appendChild(row);
    });
    
    document.getElementById("leaderboard-container").style.display = "block";
}

function fightBoss() {
    let totalEmpireStrength = calculateTotalArmyStrength();
    
    // Double the damage for ballistas
    totalEmpireStrength += army.ballista * units.ballista.strength;

    // Apply Troubadour buff
    if (army.troubadour > 0) {
        totalEmpireStrength += (army.soldier + army.archer + army.knight + army.ballista) * army.troubadour;
    }

    const damage = Math.floor(totalEmpireStrength);
    bossHealth = Math.max(0, bossHealth - damage);
    updateBossHealth();
    updateBossStats();

    if (bossHealth > 0) {
        notify(`You dealt ${damage} damage to the Dragon Emperor!`);
    } else {
        showVictoryMessage(); 
        document.getElementById('boss-button').style.display = 'none';
        return;
    }

    bossAttackCount++; 
    const bossStrength = (bossMaxHealth / 100) * (1 + bossAttackCount * 0.2);
    const bossDamage = Math.floor(bossStrength);
    
    let remainingDamage = bossDamage;
    let damageReport = {
        totalDamage: bossDamage,
        soldiersLost: 0,
        knightsLost: 0,
        troubadoursLost: 0,
        populationLost: 0
    };

    // Damage to soldiers
    if (army.soldier > 0 && remainingDamage > 0) {
        const soldierDefense = units.soldier.defense;
        const soldiersLost = Math.min(army.soldier, Math.floor(remainingDamage / soldierDefense));
        army.soldier -= soldiersLost;
        remainingDamage -= soldiersLost * soldierDefense;
        damageReport.soldiersLost = soldiersLost;
    }

    // Damage to knights
    if (army.knight > 0 && remainingDamage > 0) {
        const knightDefense = units.knight.defense;
        const knightsLost = Math.min(army.knight, Math.floor(remainingDamage / knightDefense));
        army.knight -= knightsLost;
        remainingDamage -= knightsLost * knightDefense;
        damageReport.knightsLost = knightsLost;
    }

    // Damage to troubadours
    if (army.troubadour > 0 && remainingDamage > 0) {
        const troubadourDefense = units.troubadour.defense;
        const troubadoursLost = Math.min(army.troubadour, Math.floor(remainingDamage / troubadourDefense));
        army.troubadour -= troubadoursLost;
        remainingDamage -= troubadoursLost * troubadourDefense;
        damageReport.troubadoursLost = troubadoursLost;
    }

    // Damage to population
    if (remainingDamage > 0) {
        const populationLost = Math.min(population, remainingDamage);
        population = Math.max(0, population - populationLost);
        damageReport.populationLost = populationLost;

        if (population <= 0) {
            gameOver();
        }
    }

    notify(`The Dragon Emperor attacked! Damage: ${bossDamage}`, "error");
    updateArmy();
    updatePopulation();
    
    showDamageTooltip(damageReport);
}

function showDamageTooltip(damageReport) {
    const tooltipContent = `
        <strong>Battle Report:</strong><br>
        Total Damage: ${damageReport.totalDamage}<br>
        Soldiers Lost: ${damageReport.soldiersLost}<br>
        Knights Lost: ${damageReport.knightsLost}<br>
        Troubadours Lost: ${damageReport.troubadoursLost}<br>
        Population Lost: ${damageReport.populationLost}
    `;
    
    const tooltip = document.getElementById('damage-tooltip');
    tooltip.innerHTML = tooltipContent;
    tooltip.style.display = 'block';
    
    setTimeout(() => {
        tooltip.style.display = 'none';
    }, 5000); // Hide tooltip after 5 seconds
}

function updateBossHealth() {
    const healthBar = document.getElementById('boss-health');
    const healthText = document.getElementById('boss-health-text');
    const healthPercentage = (bossHealth / bossMaxHealth) * 100;
    healthBar.style.width = `${healthPercentage}%`;
    healthText.textContent = `${Math.round(healthPercentage)}%`;
}

function updateBossStats() {
    const bossHealthStat = document.getElementById('boss-health-stat');
    const bossStrengthStat = document.getElementById('boss-strength-stat');
    
    const healthPercentage = (bossHealth / bossMaxHealth) * 100;
    bossHealthStat.innerHTML = `<strong>Dragon Emperor Health:</strong> ${Math.round(bossHealth)} / ${bossMaxHealth} (${Math.round(healthPercentage)}%)`;
    
    const bossStrength = (bossMaxHealth / 100) * (1 + bossAttackCount * 0.5);
    bossStrengthStat.innerHTML = `<strong>Dragon Emperor Strength:</strong> ${Math.round(bossStrength)} (+${bossAttackCount * 50}% increase)`;
}

function updateEmpireDefenseAndStrength() {
    const totalDefense = calculateTotalDefense();
    const totalStrength = calculateTotalArmyStrength();
    updateWallDefense();
    const empireStrengthElement = document.getElementById('empire-strength');
    empireStrengthElement.innerHTML = `
        <div class="strength-value">
            <strong>Total Empire Strength:</strong> ${totalStrength.toFixed(1)}
        </div>
    `;
}

function startResetGame() {
    Object.keys(resources).forEach(key => {
        resources[key].amount = resources[key].initialAmount;
    });
    Object.keys(army).forEach(key => {
        army[key] = 0;
    });
    population = 1000;
    bossHealth = bossMaxHealth;
    gameTime = 0;
    lastBossAttackTime = 0;
    bossAttackTimer = 60;
    hero.strength = 10;
    hero.experience = 0;
    hero.level = 1;
    hero.specializations = {
        gatherer: 0,
        healer: 0,
        fighter: 0
    };
    hasUniversity = false;
    wallDefenseMultiplier = 1; 
    populationGrowthRate = 0; 
    bossAttackCount = 0; 
    maxPopulationReached = 1000; 
    Object.keys(research).forEach(key => {
        research[key].level = 0;
    });
    document.getElementById('research-options').style.display = 'none';

    Object.keys(buildingCounts).forEach(key => {
        buildingCounts[key] = 0;
    });

    updateResources();
    updateArmy();
    updateBossHealth();
    updateEmpireDefenseAndStrength();
    updatePopulation();
    updateWallDefense();
    updateBossStats();
    updateHeroStats();
    createNeutralArmyButtons();
    updateCityVisualization(); 
    notify("Game started/reset!", "success");
    document.getElementById('boss-button').style.display = 'block';
}

function updateBossAttackTimer() {
    const minutes = Math.floor(bossAttackTimer / 60);
    const seconds = bossAttackTimer % 60;
    document.getElementById('boss-attack-timer').textContent = `Next attack in: ${String(minutes).padStart(2, '0')}:${String(seconds).padStart(2, '0')}`;
}

function updateEmpireArmyVisualization() {
    const vizContainer = document.getElementById('empire-army-viz');
    vizContainer.innerHTML = ''; 

    const svg = document.createElementNS("http://www.w3.org/2000/svg", "svg");
    svg.setAttribute("width", "100%");
    svg.setAttribute("height", "100%");

    const totalUnits = army.soldier + army.archer + army.knight + army.ballista + army.troubadour;
    const unitSize = Math.min(10, 180 / Math.sqrt(totalUnits)); 

    let x = 0;
    let y = 0;

    for (const unitType of ['soldier', 'archer', 'knight', 'ballista', 'troubadour']) {
        for (let i = 0; i < army[unitType]; i++) {
            const unitIcon = document.createElementNS("http://www.w3.org/2000/svg", "g");
            unitIcon.innerHTML = unitIcons[unitType];
            unitIcon.setAttribute("transform", `translate(${x},${y}) scale(${unitSize/50})`);
            svg.appendChild(unitIcon);

            x += unitSize;
            if (x > 190) {
                x = 0;
                y += unitSize;
            }
        }
    }

    vizContainer.appendChild(svg);
}

setInterval(() => {
    // Add experience from troubadours
    if (army.troubadour > 0) {
        hero.experience += army.troubadour;
        checkHeroLevelUp();
    }
  
    Object.keys(resources).forEach(key => {
        resources[key].amount += resources[key].perSecond;  
    });
    updateResources();
    population += populationGrowthRate; 
    updatePopulation(); 
    gameTime++;
    updateTimer();
    updateEmpireDefenseAndStrength();
    bossAttackTimer--;
    updateBossAttackTimer();
    updateHeroStats();
    if (bossAttackTimer <= 0) {
        fightBoss();
        bossAttackTimer = 60; 
    }
    if (hasUniversity && populationGrowthRate > 0) {
        population += populationGrowthRate; 
    }
    updateCityVisualization(); 
}, 1000); 
document.getElementById('start-reset-game').addEventListener('click', startResetGame);
createBuildings();
createRecruitmentButtons();
createNeutralArmyButtons();
createResearchOptions();
updateResources();
updateArmy();
updateBossHealth();
updateEmpireDefenseAndStrength();
updatePopulation();
updateBossStats();
updateHeroStats();
document.getElementById('boss-button').addEventListener('click', fightBoss);
document.getElementById('try-again-btn').addEventListener('click', function() {
    document.getElementById('game-over-box').style.display = 'none';
    startResetGame();
});
document.getElementById('restart-btn').addEventListener('click', function() {
    document.getElementById('victory-box').style.display = 'none';
    startResetGame();
});
</script>
</body></html>
