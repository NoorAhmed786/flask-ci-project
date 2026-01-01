Flask CI Project

This is a simple Flask web application integrated with GitHub Actions CI/CD workflows. The project includes a basic web server and unit tests, and it is set up to run automated tests with GitHub Actions every time code is pushed or a pull request is made.

Project Setup

1. Clone the Repository
git clone https://github.com/NoorAhmed786/flask-ci-project.git
cd flask-ci-project

2. Create a Virtual Environment

To set up the environment, you need to create a Python virtual environment:

python -m venv venv

3. Activate the Virtual Environment

On Windows (Command Prompt or PowerShell):

.\venv\Scripts\Activate


On macOS/Linux:

source venv/bin/activate

4. Install Dependencies

After activating the virtual environment, install the necessary dependencies by running:

pip install -r requirements.txt

5. Run the Application

To run the Flask application locally:

python app.py


This will start the Flask app at http://127.0.0.1:5000/.

6. Run Tests

To run the unit tests:

pytest


This will run the tests defined in test_app.py and show the results.

GitHub Actions CI/CD
1. CI Workflow

This repository is set up with GitHub Actions to automatically run unit tests on push to the main branch and on pull requests.

Workflow File: .github/workflows/ci.yml

The workflow checks out the code, installs dependencies, and runs unit tests using pytest.

It also caches dependencies for faster builds.

2. Self-Hosted Runner

To use a self-hosted GitHub Actions runner, follow these steps:

Set up a self-hosted runner on a local machine, VM, or Raspberry Pi.

Register the runner with GitHub following the instructions in the GitHub Actions settings.

Once the runner is set up, GitHub Actions will automatically use it to run workflows.

3. Security Considerations

Please review the runner-security.md file for security considerations when using self-hosted runners.

Project Structure

app.py: The main Flask application file.

test_app.py: Unit tests for the Flask application using pytest.

.github/workflows/ci.yml: GitHub Actions CI workflow configuration.

requirements.txt: Python dependencies (Flask, pytest, etc.).

runner-setup/: Folder containing scripts and logs for the self-hosted runner setup.

runner-setup.sh: Script to install and configure the self-hosted runner.

runner-service-logs.txt: Logs for the self-hosted runner service.

runner-security.md: Security considerations for self-hosted runners.

License

This project is licensed under the MIT License - see the LICENSE
 file for details.