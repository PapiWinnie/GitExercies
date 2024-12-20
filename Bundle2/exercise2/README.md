# Checkout your main branch and pull the latest changes
git checkout main
git pull origin main

# Create a new branch named 'ft/service-redesign'
git checkout -b ft/service-redesign

# Add new changes to the service.html page
echo "<!DOCTYPE html><html><head><title>Service</title></head><body><h1>Service Redesign</h1><p>Updated services description.</p></body></html>" > service.html

# Stage, commit, and push the changes
git add service.html
git commit -m "Redesign the services page"
git push -u origin ft/service-redesign

# Create a new Pull Request (PR) for your changes
# (This step typically requires you to go to your GitHub repository in a web browser)
# Navigate to the "Pull Requests" tab, click "New Pull Request",
# select 'ft/service-redesign' as the compare branch and 'main' as the base branch,
# then click "Create Pull Request".

# Go back to your main branch and add new changes to service.html
git checkout main
echo "<!DOCTYPE html><html><head><title>Service</title></head><body><h1>Updated Services Section</h1><p>New description for services.</p></body></html>" >> service.html

# Stage, commit, and push those changes
git add service.html
git commit -m "Update services section in main"
git push origin main

# Check the GitHub PR for conflicts with the main branch.
# You will see that there are merge conflicts due to changes in the same part of service.html.

# In your project, checkout the 'ft/service-redesign' branch again
git checkout ft/service-redesign

# Compare 'ft/service-redesign' with 'main' branch using git diff
git diff main

# Merge the main branch into 'ft/service-redesign' branch and resolve conflicts
git merge main

# If there are conflicts, Git will show them. Open service.html in your editor,
# resolve the conflicts manually by choosing how to integrate both sets of changes,
# then stage the resolved file:
git add service.html

# Commit the merge changes
git commit -m "Merge main into ft/service-redesign and resolve conflicts"

# Push the merged changes back to the remote repository
git push origin ft/service-redesign
