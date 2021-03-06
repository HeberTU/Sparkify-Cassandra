# Sparkify-Cassandra
[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)

Code for project: Sparkify, Udacity

- Origin: (https://github.com/HeberTU/Sparkify-Cassandra)
- Author: Heber Trujillo <heber.trj.urt@gmail.com>
- Date of last README.md update: 21.02.2022

## Project Overview

### Motivation

A startup called Sparkify wants to analyze the data they've been collecting on 
songs and user activity on their new music streaming app. The analysis team is 
particularly interested in understanding what songs users are listening to. Currently,
there is no easy way to query the data to generate the results, since the data reside 
in a directory of CSV files on user activity on the app.

This project aims to show Python capabilities for data modeling and ETL
pipelines design using [Apache Cassandra](https://cassandra.apache.org/_/index.html).

Mainly, this project will focus on:

* Define table structure, Partition key, and Clustering Columns based on the queries demanded by the analysis team.
* ETL pipeline design to transfer data from two local directories to a Cassandra Data Base.

## How to Run Scripts 

### Dependencies Installation 

1. Poetry is the tool used for dependency management. To install poetry, run from a terminal:
    ```bash
    pip install poetry
    ```
    Make sure that version 1.1.8 is installed (1.1.7 is buggy).
2. Create and activate a virtual environment for the project. For example:
    ```bash
    python3 -m venv ./.venv
    ./.venv/Scripts/activate
    ```
3. From the virtual environment, install the required dependencies with
    ```bash
    poetry update
    ```
### Cassandra Installation

If you are working on Windows, you can follow the steps described in the 
following [video](https://www.youtube.com/watch?v=-1waKtjNt88).

### Scripts

The project contains a single notebook file, which the following structure:

* Part I: ETL Pipeline for Pre-Processing the Files.
* Part II: Data Modeling with Cassandra

## Data

The available data consists of:

* Event Data: User generated data, which after processing contains the following structure:
  * artist 
  * firstName of user 
  * gender of user 
  * item number in session 
  * last name of user 
  * length of the song 
  * level (paid or free song)
  * location of the user 
  * sessionId 
  * song title 
  * userI