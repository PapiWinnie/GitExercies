# Create a new branch named 'ft/bundle-2' and switch to it
git checkout -b ft/bundle-2

# Create a new page named services.html and add some HTML content
echo "hello" > services.html

# Stage the new file for commit
git add services.html

# Commit the changes with a descriptive message
git commit -m "Add services page"

# Push the new branch to the remote repository
git push -u origin ft/bundle-2

# Create a Pull Request against the 'main' branch on GitHub

