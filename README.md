# Task 2 - Number Guessing Game

## Branch Structure

This project uses multiple Git branches to develop, test, and commit features independently
of one another.

### main: 
- Initial stable version of the game
### feature1: 
- Adds quit and play-again functionality as well as user feedback messages
### feature2: 
- Adds a condition for maximum attempts and a game over state
### feature3: 
- Adds a hint-related functionality
### hotfix:
- Fixes an error in random number generation over the intended range
### dev: 
- Serves as an integration branch for features

## Learning Summary
### Merge
- Combines two branches into one commit (or fast-forwards if possible)
- Keeps the whole commit history from the feature branch
- Ideally, fully merged branches are deleted after merging unless needed
- Safer, slower, more methodical for team settings, I would think

### Rebase
- Reapplies commits from one branch into another
- Keeps history linear and clean, avoids unnecessary merge commits
- The downside is that you lose the code history of the merged branch
- Seems ideal for merging recent updates from dev into feature branches before merging them
- Best-suited for solo projects or ones unlikely to have many people working on branches

### Squash
- Combines multiple commits into a single commit
- Cleans up messy history within features, reducing clutter and keeping history readable
- Useful before merging long-running feature branches

### Cherry-pick
- Applies a single commit from another branch without merging the whole branch
- Ideal for urgent hotfixes

### Observations From the Git History
- feature1: merged with dev directly; history shows multiple commits
- feature2: merged after updating with dev; history just shows clean merge
- feature3: multiple commits squashed before merging; history shows only one clean commit
- hotfix:   cherry-picked changes into main, then merged to dev, commit shown for each

### When I Would Use Each Projects
- Merge:       For any time I want to integrate routine features into other branches
- Rebase:      For when I want to maintain a clean, linear history on feature branches, and I'm 
               not worried about others modifying
- Squash:      For when I want to clean up a lot of messy commits before sharing or merging
- Cherry-pick: For any urgent fixes that pop up that I want to quickly move into main or 
               do selective commits across branches