# Stellar Burgers Unit Tests

Unit test suite for the core domain logic of the Stellar Burgers ordering service — `Bun`, `Ingredient`, `Burger`, and `Database` classes.

**Tech:** Python · Pytest · pytest-cov

## Coverage

100% line coverage across all four domain classes:


`Bun` — bun creation and price/name access
`Ingredient` — ingredient typing and pricing
`Burger` — composition logic, ingredient management, total price calculation
`Database` — available buns and ingredients


Coverage verified via `pytest-cov` HTML report.

## Project Structure

```
praktikum/     # Application code under test
tests/         # Unit tests grouped by class
               # bun_test.py, ingredient_test.py, burger_test.py, database_test.py
```

## Run

```bash
pip install -r requirements.txt

# Run tests with HTML coverage report
pytest --cov=praktikum --cov-report=html

# Open report
open htmlcov/index.html
```

## Test Approach


One test module per domain class — clear mapping to source code
Parametrized tests for boundary conditions and varying inputs
Mock-free where possible — tests run against real domain objects for fidelity
