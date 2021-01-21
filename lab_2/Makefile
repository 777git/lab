.DEFAULT_GOAL := all

all: install test run deploy

install:
	@echo "Installing pipenv and dependencies.";
	pip install pipenv;	 	
	pipenv --python 3.7;
	
	
	pipenv install requests;
	pipenv install ntplib;

	pipenv install pytest;	

test:
	@echo "Start tests.";
	pipenv run python3 -m pytest ./tests/tests.py

run:
	@echo "Run Python app."
	python3 -m pipenv run python app.py

deploy:
	@echo "Adding and Committing results.txt to git.";
	#python3 -m pipenv run pytest ./tests/tests.py > results.txt; python3 -m pipenv run python app.py >> results.txt
	git add ./results.txt;
	git commit -m "Lab2: deploy through make";
	git push origin main