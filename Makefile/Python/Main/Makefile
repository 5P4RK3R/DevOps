# Define variables
PYTHON = python3
PIP = pip3
VENV = venv

# Define targets
.PHONY: all install clean run

# Default target to set up the environment and run the server
all: install run

# Install dependencies
install:
	$(PYTHON) -m venv $(VENV)
	. $(VENV)/bin/activate && $(PIP) install -r requirements.txt

# Clean the project
clean:
	rm -rf $(VENV)
	find . -type f -name "*.pyc" -delete
	find . -type d -name "__pycache__" -delete

# Run the server
run:
	. $(VENV)/bin/activate && $(PYTHON) main.py
	