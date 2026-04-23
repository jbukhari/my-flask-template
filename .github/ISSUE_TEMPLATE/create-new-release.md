---
name: Create new release
about: Tasks required to cut a new release

---

- [ ] Ensure all issues in the milestone are closed or moved to another milestone
- [ ] In a new branch, update the version in config.py and wherever else it appears
- [ ] Create the release from the new branch using a tag named after the version
- [ ] Open a PR updating config.py in the main branch with the new version + "dev"  
