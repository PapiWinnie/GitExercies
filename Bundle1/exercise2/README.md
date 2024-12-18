# Create a new home.html file, add HTML content, and save it
echo "hello" > home.html

# Stash the changes for home.html
git stash push -m "Stashed changes for home.html"

# Incase when stashing doesn't work first add the file to stage area

git add home.html
git stash push -m "stashed home.html"

# Create a new about.html file, add HTML content, and save it
echo "file about.html" > about.html

# Stash the changes for about.html
git stash push -m "Stashed changes for about.html"

# Create a new team.html file, add HTML content, and save it
echo "team.html" > team.html

# Stash the changes for team.html
git stash push -m "Stashed changes for team.html"

# Restore the changes of the about.html page
git stash pop stash@{1}

# Restore the changes of the home.html page using index
git stash pop stash@{0}

# Commit the current changes (home.html and about.html)
git add home.html about.html
git commit -m "Added home and about pages"

# Push the committed changes to GitHub
git push origin main
  

# Reset the current changes to go back to the state without team.html page
git reset --hard HEAD~1  # This will remove the last commit including team.html changes
