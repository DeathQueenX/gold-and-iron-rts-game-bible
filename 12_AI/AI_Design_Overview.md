# AI Design Overview

## Purpose

AI-ul trebuie să poată susține skirmish, campanie, co-op și scenarii dinamice. Nu trebuie să fie doar un build-order bot; trebuie să joace conform identității facțiunii.

## AI layers

### 1. Economy AI
Decide worker production, expansion timing, resource priorities and rebuilding behavior.

### 2. Military AI
Decide army composition, attack waves, defense, retreats and harassment.

### 3. Map Control AI
Decide captures of mines, ports, shrines, trade lanes, relics and chokepoints.

### 4. Hero AI
Controls hero leveling, ability timing, retreat thresholds and item usage.

### 5. Crisis AI
Controls Ashlands pulses, boss spawns, corruption spread and neutral aggression.

## Faction AI personalities

### Ferrum AI
- expands slowly;
- heavily fortifies resource nodes;
- favors infantry and siege;
- counterattacks after holding an enemy push;
- prioritizes mines and chokepoints.

### Aurelia AI
- expands through roads and shrines;
- uses formation armies;
- prioritizes sunstone;
- casts solar abilities on clustered enemies;
- prefers clean, direct pushes.

### Thalassia AI
- expands through ports;
- harasses trade and workers;
- uses naval superiority;
- avoids dry central fights unless ahead;
- prioritizes mobility and mist.

### Ashlands AI
- does not play like standard AI;
- spreads corruption;
- guards relics;
- sends pulse waves;
- reacts to Abyssal Crystal exploitation.

## Difficulty model

### Easy
- slower economy;
- limited micro;
- delayed hero abilities;
- fewer simultaneous attacks.

### Normal
- standard economy;
- moderate army composition logic;
- uses heroes and objectives.

### Hard
- stronger map awareness;
- better counters;
- coordinated attacks;
- objective pressure.

### Brutal
- optimized build orders;
- multi-pronged attacks;
- high hero micro;
- aggressive expansions;
- does not require unfair hidden information unless explicitly enabled.

## AI fairness rules

- AI should not see through fog unless difficulty rules say so.
- AI should scout before countering.
- AI should retreat valuable heroes.
- AI should rebuild production if destroyed.
- AI should adapt after repeated losses.
