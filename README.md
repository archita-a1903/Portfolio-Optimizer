# Portfolio-Optimizer

This project is a command-line tool for portfolio optimization using the knapsack algorithm. It selects a set of assets from a CSV file to maximize expected return under a capital constraint and risk tolerance. It can also plot the efficient frontier.

## Files

- `main.py`: Main script for portfolio optimization.
- `assets.csv`: Example asset data.
- `frontier.png`: Output plot of the efficient frontier (generated if plotting is enabled).

## Usage

Run the optimizer from the command line:

```sh
python main.py --capital <amount> --risk <max risk score> --csv assets.csv [--plot]
```

- `--capital`: Total capital available for investment (integer).
- `--risk`: Maximum allowed risk score per asset (integer, 0-100).
- `--csv`: Path to the asset CSV file.
- `--plot`: (Optional) Generate and save the efficient frontier plot as `frontier.png`.

### Example

```sh
python main.py --capital 10000 --risk 50 --csv assets.csv --plot
```

## CSV Format

The CSV file should have the following columns:

- `Ticker`: Asset symbol
- `ExpectedReturn(%)`: Expected return in percent
- `RiskScore(0-100)`: Risk score (0-100)
- `Price`: Price per asset

## Output

- Prints selected assets, total cost, expected return, and average risk score.
- If `--plot` is used, saves the efficient frontier plot as `frontier.png`.

## Requirements

- Python 3.x
- matplotlib

Install dependencies with:

```sh
pip install matplotlib
```

## Demo Video

You can find the demo of how to use this with this YouTube link: https://youtu.be/fEeCrZnBBgM. I havve explained various aspects of the project within here

## License
MIT License
