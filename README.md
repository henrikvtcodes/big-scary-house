# Big Scary House
Welcome to Big Scary House: I created this because I decided to turn my house into an interactive halloween fixture. This monorepo holds all the code for all the components. BSH is a system to set up a house for various interactive demonstrations.

## Monorepo Components
- `core`: This folder contains a webserver (Python/FastAPI or Typescript/Express) that is the main orchestrator. It is responsible for managing everything such as lighting, movements, sound, etc.
- `motion`: This folder contains of the many Lua components that are designed to be compiled and run as workers. Motion is responsible for handling worker nodes that have 1+ PIR sensors attached. These nodes are most commonly used to monitor for motion in a certain area and then trigger the core server to perform another action.

## Tools
There are a few tools that are prerequisites to deploying or contributing to this project. 
- Node.js / NPM: These tools are required in order to run the `core` server. It is also highly recommended to install it because this project is not plug and play; configuration is required.
- Yarn: This is what `core` uses for packagage management. Please do not use NPM cli if you intend to contribute, as your PR will not be merged.
- `nodemcu-tool`: This is a NodeJS based CLI tool created by the NodeMCU team for the purpose of executing Lua and uploading Lua to an ESP32 with NodeMCU firmware.

## Recommended Hardware
This system is designed to use a Raspberry Pi 2B and up for the core controller and ESP-32's running NodeMCU as the worker/remote nodes. 