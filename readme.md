# Uber-like Backend

**This repository contains a simple backend application that demonstrates how an app like Uber works. It includes the basic functionality for a ride-hailing service such as requesting a ride, matching drivers with riders, and tracking the progress of the ride.**

## Getting Started

To run the application, you will need to run the node and db services with the command `docker-compose up -d`. These service will initialize a container named `driveapp` and another named `driveappdb`.

Install the dependencies inside the `driveapp` container with `npm install`.

## Running the Application

To start the application, you will need to run the following command: `npm start`

This will start the server and you will be able to access the application at [http://localhost:3001](http://localhost:3001/).

##  Available Drivers

Check available drivers by making a GET request to the endpoint `/open/travels`.

## Requesting a Ride

To request a ride, a user will need to make a POST request to the endpoint`/:passengerId/request/travel`.

## Accepting a Ride

Once a driver receives a ride request, they will have the option to accept or reject the ride. To accept the ride, the driver will need to make a PUT request to the endpoint `/:driverId/travels/:travelId/start`.

## Completing the Ride

When the driver arrives at the destination, they will mark the ride as complete by making a PUT request to the endpoint `/:driverId/travels/:travelId/end`.


> **This application serves as a simple example of how a ride-hailing service can be implemented with a backend server. It can be used as a
> starting point for building more complex applications.**
