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
    padding: 20px;
    overflow-y: auto;
}
.main-area {
    flex-grow: 1;
    padding: 20px;
    overflow-y: auto;
    display: flex;
    flex-direction: column;
}
h1, h2 {
    margin-top: 0;
    color: #f39c12;
}
.resource, .unit {
    margin-bottom: 10px;
    padding: 10px;
    background: rgba(255,255,255,0.1);
    border-radius: 5px;
}
.building, .recruit-btn, #boss-button {
    display: inline-block;
    width: 100px;
    height: 100px;
    margin: 10px;
    background: rgba(255,255,255,0.2);
    border-radius: 10px;
    text-align: center;
    cursor: pointer;
    transition: transform 0.3s ease;
}
.building:hover, .recruit-btn:hover, #boss-button:hover {
    transform: scale(1.05);
}
.building img, .recruit-btn img {
    width: 60px;
    height: 60px;
    margin-top: 10px;
}
.cost {
    position: absolute;
    bottom: 5px;
    left: 5px;
    right: 5px;
    background: rgba(0,0,0,0.7);
    color: white;
    font-size: 0.8em;
    padding: 2px;
    border-radius: 3px;
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
    font-size: 1.2em;
    width: 200px;
    height: 60px;
    line-height: 60px;
    margin-top: 20px;
}
#boss-health-bar {
    width: 100%;
    height: 20px;
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
    line-height: 20px;
    color: white;
    font-weight: bold;
}
#timer {
    font-size: 1.2em;
    margin-bottom: 10px;
    color: #f39c12;
}
.building, .recruit-btn {
    position: relative;
}
.defense-value, .strength-value {
    margin-bottom: 10px;
    padding: 10px;
    background: rgba(255,255,255,0.1);
    border-radius: 5px;
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
    margin-bottom: 20px;
    padding: 10px;
    background: rgba(255,255,255,0.1);
    border-radius: 5px;
}
#boss-stats div {
    margin-bottom: 5px;
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
        <h2>Boss Attack Timer</h2>
        <div id="boss-attack-timer">Next attack in: 02:00</div>
    </div>
    <div class="main-area">
        <h2>Buildings</h2>
        <div id="buildings">
            <!-- Buildings will be dynamically added here -->
        </div>
        <h2>Recruitment</h2>
        <div id="recruitment">
            <!-- Recruitment buttons will be dynamically added here -->
        </div>
        <h2>Empire Defense and Strength</h2>
        <div id="empire-defense"></div>
        <div id="empire-strength"></div>
        <h2>Boss Stats</h2>
        <div id="boss-stats">
            <div id="boss-health-stat"></div>
            <div id="boss-strength-stat"></div>
        </div>
        <h2>Boss Battle</h2>
        <div id="boss-battle">
            <div id="boss-button">Fight the Boss!</div>
            <div id="boss-health-bar">
                <div id="boss-health"></div>
                <div id="boss-health-text">100%</div>
            </div>
        </div>
    </div>
</div>
<div id="notification-area"></div>
<div id="defense-page">
    <h2>Empire Defense and Strength</h2>
    <div id="empire-stats"></div>
    <div id="boss-info">
        <h3>Boss Information</h3>
        <div id="boss-strength"></div>
        <div id="boss-attack-timer"></div>
    </div>
    <button id="back-to-main">Back to Main Page</button>
</div>
<script>
const resources = {
    gold: { name: "Gold", amount: 1000, perSecond: 1, initialAmount: 1000 },
    wood: { name: "Wood", amount: 500, perSecond: 2, initialAmount: 500 },
    stone: { name: "Stone", amount: 300, perSecond: 1, initialAmount: 300 },
    food: { name: "Food", amount: 1000, perSecond: 5, initialAmount: 1000 },
    iron: { name: "Iron", amount: 200, perSecond: 1, initialAmount: 200 }
};

const buildings = {
    mine: { name: "Gold Mine", cost: { gold: 20, wood: 10 }, produces: { gold: 100 } },
    lumbermill: { name: "Lumber Mill", cost: { gold: 15, wood: 50 }, produces: { wood: 200 } },
    quarry: { name: "Stone Quarry", cost: { gold: 25, wood: 15 }, produces: { stone: 100 } },
    farm: { name: "Farm", cost: { gold: 10, wood: 10 }, produces: { food: 300 } },
    ironmine: { name: "Iron Mine", cost: { gold: 300, wood: 200 }, produces: { iron: 100 } },
    university: { name: "University", cost: { gold: 200, wood: 200, stone: 100 }, produces: {} },
    wall: { name: "Wall", cost: { stone: 50, wood: 20 }, defense: 10 }
};

let wallDefense = 0;

const units = {
    soldier: { name: "Soldier", cost: { gold: 50, food: 20 }, strength: 5, defense: 3, upgradeBonus: { strength: 1, defense: 1 } },
    archer: { name: "Archer", cost: { food: 70, wood: 30 }, strength: 7, defense: 2, upgradeBonus: { strength: 2, defense: 0.5 } },
    knight: { name: "Knight", cost: { food: 100, iron: 50 }, strength: 10, defense: 8, upgradeBonus: { strength: 2, defense: 2 } },
    siege: { name: "Siege Engine", cost: { gold: 200, wood: 100, iron: 50 }, strength: 15, defense: 5, upgradeBonus: { strength: 3, defense: 1 } }
};

const army = {
    soldier: 0,
    archer: 0,
    knight: 0,
    siege: 0
};

let population = 10000; // Starting population
let bossHealth = 10000;
const bossMaxHealth = 10000;
let gameTime = 0;
let lastBossAttackTime = 0;
let bossAttackTimer = 120; // 2 minutes in seconds

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
    populationElement.innerHTML = `<div class="resource"><strong>Population:</strong> ${population}</div>`;
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
}

function createBuildings() {
    const buildingsContainer = document.getElementById('buildings');
    Object.keys(buildings).forEach(key => {
        const building = buildings[key];
        const buildingElement = document.createElement('div');
        buildingElement.className = 'building';
        buildingElement.innerHTML = `
            <img alt="${building.name} icon" src="${key}.svg" width="60" height="60">
            <div>${building.name}</div>
            <div class="cost">${formatCost(building.cost)}</div>
        `;
        buildingElement.onclick = () => buyBuilding(key);
        buildingsContainer.appendChild(buildingElement);
    });
}

function createRecruitmentButtons() {
    const recruitmentContainer = document.getElementById('recruitment');
    Object.keys(units).forEach(key => {
        const unit = units[key];
        const buttonElement = document.createElement('div');
        buttonElement.className = 'recruit-btn';
        buttonElement.innerHTML = `
            <img alt="${unit.name} icon" src="${key}.svg" width="60" height="60">
            <div>${unit.name}</div>
            <div class="cost">${formatCost(unit.cost)}</div>
        `;
        buttonElement.onclick = () => recruitUnit(key);
        recruitmentContainer.appendChild(buttonElement);
    });
}

function buyBuilding(buildingKey) {
    const building = buildings[buildingKey];
    if (canAfford(building.cost)) {
        Object.keys(building.cost).forEach(resource => {
            resources[resource].amount -= building.cost[resource];
        });
        if (buildingKey === 'wall') {
            wallDefense += building.defense;
        } else {
            Object.keys(building.produces).forEach(resource => {
                resources[resource].perSecond += building.produces[resource];
            });
        }
        updateResources();
        updateWallDefense();
        notify(`${building.name} purchased!`);
    } else {
        notify("Not enough resources!", "error");
    }
}

function updateWallDefense() {
    const empireDefenseElement = document.getElementById('empire-defense');
    empireDefenseElement.innerHTML = `
        <div class="defense-value">
            <strong>Wall Defense:</strong> ${wallDefense}
        </div>
        ${empireDefenseElement.innerHTML}
    `;
}

function recruitUnit(unitKey) {
    const unit = units[unitKey];
    if (canAfford(unit.cost)) {
        Object.keys(unit.cost).forEach(resource => {
            resources[resource].amount -= unit.cost[resource];
        });
        army[unitKey]++;
        updateResources();
        updateArmy();
        notify(`${unit.name} recruited!`);
    } else {
        notify("Not enough resources to recruit!", "error");
    }
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

function fightBoss() {
    const totalEmpireStrength = Object.keys(army).reduce((sum, unit) => {
        return sum + army[unit] * units[unit].strength;
    }, 0);
    
    const damage = Math.floor(totalEmpireStrength * (Math.random() * 0.5 + 0.75));
    bossHealth = Math.max(0, bossHealth - damage);
    updateBossHealth();
    updateBossStats();

    if (bossHealth > 0) {
        notify(`You dealt ${damage} damage to the boss! Take that bad boy down`);
    } else {
        notify("Congratulations! You've defeated the boss and won the game!", "success");
        document.getElementById('boss-button').style.display = 'none';
        return;
    }

    const bossStrength = bossMaxHealth / 100;
    const bossDamage = Math.floor(bossStrength * (Math.random() * 0.5 + 0.75));
    
    let remainingDamage = bossDamage;

    // Attack walls first
    if (wallDefense > 0) {
        const wallDamageTaken = Math.min(wallDefense, remainingDamage);
        wallDefense -= wallDamageTaken;
        remainingDamage -= wallDamageTaken;
    }

    // Attack soldiers
    if (remainingDamage > 0 && army.soldier > 0) {
        const soldierDefense = units.soldier.defense * army.soldier;
        const soldierDamageTaken = Math.min(soldierDefense, remainingDamage);
        const soldiersLost = Math.ceil(soldierDamageTaken / units.soldier.defense);
        army.soldier -= soldiersLost;
        remainingDamage -= soldierDamageTaken;
    }

    // Attack archers
    if (remainingDamage > 0 && army.archer > 0) {
        const archerDefense = units.archer.defense * army.archer;
        const archerDamageTaken = Math.min(archerDefense, remainingDamage);
        const archersLost = Math.ceil(archerDamageTaken / units.archer.defense);
        army.archer -= archersLost;
        remainingDamage -= archerDamageTaken;
    }

    // Damage population if there's remaining damage
    if (remainingDamage > 0) {
        const populationLost = Math.min(population, Math.ceil(remainingDamage));
        population -= populationLost;

        if (population <= 0) {
            gameOver();
        }
    }

    notify(`The boss attacked!`, "error");
    updateArmy();
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
    bossHealthStat.innerHTML = `<strong>Boss Health:</strong> ${Math.round(bossHealth)} / ${bossMaxHealth} (${Math.round(healthPercentage)}%)`;
    
    const bossStrength = bossMaxHealth / 100;
    bossStrengthStat.innerHTML = `<strong>Boss Strength:</strong> ${Math.round(bossStrength)}`;
}

function updateEmpireDefenseAndStrength() {
    const totalDefense = wallDefense + Object.keys(army).reduce((sum, unit) => {
        return sum + army[unit] * units[unit].defense;
    }, 0);

    const totalStrength = Object.keys(army).reduce((sum, unit) => {
        return sum + army[unit] * units[unit].strength;
    }, 0);

    const empireDefenseElement = document.getElementById('empire-defense');
    empireDefenseElement.innerHTML = `
        <div class="defense-value">
            <strong>Total Empire Defense:</strong> ${totalDefense.toFixed(1)}
        </div>
    `;

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
    population = 10000;
    bossHealth = bossMaxHealth;
    gameTime = 0;
    lastBossAttackTime = 0;
    bossAttackTimer = 120;

    updateResources();
    updateArmy();
    updateBossHealth();
    updateEmpireDefenseAndStrength();
    updatePopulation();
    updateWallDefense();
    updateBossStats();
    notify("Game started/reset!", "success");
    document.getElementById('boss-button').style.display = 'block';
}

function updateBossAttackTimer() {
    const minutes = Math.floor(bossAttackTimer / 60);
    const seconds = bossAttackTimer % 60;
    document.getElementById('boss-attack-timer').textContent = `Next attack in: ${String(minutes).padStart(2, '0')}:${String(seconds).padStart(2, '0')}`;
}

document.getElementById('start-reset-game').addEventListener('click', startResetGame);
createBuildings();
createRecruitmentButtons();
updateResources();
updateArmy();
updateBossHealth();
updateEmpireDefenseAndStrength();
updatePopulation();
updateBossStats();
setInterval(() => {
    Object.keys(resources).forEach(key => {
        resources[key].amount += resources[key].perSecond / 10;  
    });
    updateResources();
    updatePopulation();
    gameTime++;
    updateTimer();
    updateEmpireDefenseAndStrength();
    bossAttackTimer--;
    updateBossAttackTimer();
    if (bossAttackTimer <= 0) {
        fightBoss();
        bossAttackTimer = 120; // Reset timer after attack
    }
}, 1000);
document.getElementById('boss-button').addEventListener('click', fightBoss);
</script>
</body></html>
