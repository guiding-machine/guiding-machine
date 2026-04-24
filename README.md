# Guiding-Machine
A machine that provides guidance.

In order to launch it from the command line or as a Python subprocess:
```bash
echo "Theodotos-Alexandreus: How do we do it? Provide guidance, machine." \
  | uvx guiding-machine \
    --provider-api-key=sk-proj-... \
    --github-token=ghp_... 
```

Or, with a local pip installation:
```bash
pip install guiding-machine
```
Set the environment variables:
```bash
export PROVIDER_API_KEY="sk-proj-..."
export GITHUB_TOKEN="ghp_..."
```
Then:
```bash
guiding-machine multilogue.txt
```
Or:
```bash
guiding-machine multilogue.txt new_turn.txt
```
Or:
```bash
cat multilogue.txt | guiding-machine
```
Or:
```bash
cat multilogue.txt | guiding-machine > tmp && mv tmp multilogue.txt
```
Or: 
```bash
(cat multilogue.txt; echo:"Theodotos: What do you think, Guiding-Machine?") \
  | guiding-machine
```
Or:
```bash
cat multilogue.txt new_turn.txt | guiding-machine
```
Or:
```bash
cat multilogue.txt new_turn.txt | guiding-machine >  tmp && mv tmp multilogue.txt
```
Or, if you have installed other machines:
```bash
cat multilogue.md | guiding-machine \
  | summarizing-machine | judging-machine > summary_judgment.md
```

Or use it in your Python code:
```Python
# Python
import guiding_machine
```
