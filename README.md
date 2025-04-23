# EvoDriveAI


**EvoDriveAI** is a Python-based simulation showcasing AI-driven autonomous vehicles navigating a procedurally generated wavy track. These vehicles are powered by evolving neural networks, optimized using genetic algorithms. Built with **Pygame**, this project is a hands-on exploration of artificial intelligence, neural networks, and evolutionary computation within a visual simulation environment.

## Table of Contents

1. [Features](#features)  
2. [Code Structure](#code-structure)  
3. [Controls](#controls)  
4. [How It Works](#how-it-works)  
5. [License](#license)

## Features

- 🚗 **Autonomous Vehicles**: Self-driving cars controlled by neural networks that evolve over generations.
- 🌊 **Dynamic Track Generation**: Wavy road with randomly generated curves to challenge the AI.
- 🔎 **Sensor-Based Navigation**: Vehicles are equipped with simulated sensors to detect boundaries and avoid collisions.
- 🧠 **Real-Time Neural Network Visualization**: Watch the decision-making process of the top-performing car's neural network.
- 💾 **Save/Load Intelligence**: Save and reload the most effective neural network across sessions.

## Code Structure

- `car.py`: Handles car movement, neural network decisions, and sensor feedback.  
- `controls.py`: Manages user input during simulation runtime.  
- `main.py`: The core simulation loop and rendering logic.  
- `network.py`: Defines the architecture and operations of the neural networks.  
- `road.py`: Generates the dynamic wavy road and manages its rendering.  
- `sensor.py`: Simulates ray-based sensors for obstacle detection.  
- `settings.py`: Centralized configuration for the simulation environment.  
- `visualizer.py`: Visual output for neural network activity.  
- `save_state.json`: Stores the most successful neural network and its generation count.

## Controls

- `R`: Restart the simulation with a new generation (mutated from the best performer).  
- `S`: Save the current best neural network (if superior to the previous save).  
- `ESC`: Exit the simulation, saving the current best network automatically if available.

## How It Works

### Neural Network

Each vehicle is powered by a **feedforward neural network**. This network processes sensor inputs and makes movement decisions in real time.

- **Input Layer**: Distances from road borders, captured via simulated sensors, are normalized and passed to the network.  
- **Hidden Layers**: Intermediate layers analyze input data using weighted sums and activation functions to detect patterns.  
- **Output Layer**: Four control signals—forward, left, right, reverse—determine how the car moves.

### Genetic Algorithm

The AI improves through evolutionary strategies:

- **Initialization**: The simulation starts with a population of vehicles with randomized neural networks.  
- **Fitness Evaluation**: Performance is scored based on distance traveled without crashing.  
- **Selection**: The highest-scoring vehicle is selected as the genetic base for the next generation.  
- **Mutation**: Its neural network is copied and slightly mutated to introduce new behaviors.  
- **Evolution**: This cycle repeats, allowing the AI to progressively learn better driving strategies.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
