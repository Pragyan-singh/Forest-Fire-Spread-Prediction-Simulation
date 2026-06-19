# Commands to run Forest-Fire-Prediction locally

# 1. Ensure pyenv is set up (only once per machine)
# (Skip if pyenv is already installed and in your PATH)
curl https://pyenv.run | bash
# Then add to ~/.bashrc:
#   export PATH="$HOME/.pyenv/bin:$PATH"
#   eval "$(pyenv init -)"
#   eval "$(pyenv virtualenv-init -)"
# And reload shell:
#   source ~/.bashrc

# 2. Install Python 3.10.14 (only once)
pyenv install 3.10.14

# 3. Select Python 3.10.14 for this project
cd "/home/pragyan-singh/Downloads/Forest-Fire-Prediction-master"
pyenv local 3.10.14

# 4. Create and activate virtual environment (first time)
python -m venv venv310
source venv310/bin/activate

# 5. Install dependencies (first time, or when requirements.txt changes)
pip install --upgrade pip
pip install -r requirements.txt

# 6. Activate venv on subsequent runs
cd "/home/pragyan-singh/Downloads/Forest-Fire-Prediction-master"
source venv310/bin/activate

# 7. Run the Flask app
python app.py

# 8. Open in browser
# Go to: http://127.0.0.1:5000/