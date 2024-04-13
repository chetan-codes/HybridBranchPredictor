# Hybrid Branch Predictor

## Overview
This project implements a Hybrid Branch Predictor in C++ using bimodal and gshare predictors. It analyzes trace files to predict branch outcomes and evaluates misprediction rates. The hybrid approach combines the strengths of bimodal and gshare predictors for improved accuracy.

## Contents
- `main.cpp`: C++ source code implementing the hybrid branch predictor.
- `trace.txt`: Sample trace file containing hexadecimal addresses and branch outcomes.

## Features
- **Bimodal Predictor**: Implements a bimodal predictor with adjustable table size (`m2`).
- **GShare Predictor**: Implements a gshare predictor with adjustable history length (`m1`) and global history register length (`n`).
- **Hybrid Approach**: Combines bimodal and gshare predictors using a chooser table (`k`) to select the best prediction.

## Usage
1. Compile the source code using a C++ compiler: `g++ main.cpp -o sim`.
2. Run the executable with the desired predictor type and parameters:
   - Bimodal: `./sim bimodal <m2> <traceFile>`
   - GShare: `./sim gshare <m1> <n> <traceFile>`
   - Hybrid: `./sim hybrid <k> <m1> <n> <m2> <traceFile>`
3. View the prediction results and misprediction rates.

## Command Line Arguments
- `<m2>`: Size of the bimodal predictor table.
- `<m1>`: Size of the gshare predictor table.
- `<n>`: Length of the global history register.
- `<k>`: Size of the chooser table.
- `<traceFile>`: Path to the trace file containing branch addresses and outcomes.

## Output
- Number of predictions.
- Number of mispredictions.
- Misprediction rate (%).
- Final contents of the chosen predictor tables.

## Requirements
- C++ compiler (e.g., g++)
- Sample trace file for testing

## Contributors
- [Chetan Choudhary](https://github.com/chetan-codes)
- [Travis Miller](https://github.com/travismiller22)

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
