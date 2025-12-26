# Exercise Outcomes Submission Template

**Student/Group Name**: Alhambra Espigares
**Level Completed**: intermediate 
**Date**: 27-12-2025

---

## 📋 Exercise Summary

### Exercise: Intermediate Level
**Status**: ✅ Completed 

**What I did**:
I completed the exercise focused on branching, merging, resolving merge conflicts, and tagging. I created two feature branches from the intermediate branch, introduced conflicting changes in the same file, resolved the merge conflict manually, and successfully merged both branches. I also created and compared annotated and lightweight Git tags and pushed the annotated tag to the remote repository.

**Commands Used**:
```bash
git checkout -b intermediate origin/intermediate
git checkout -b feature/header
git checkout -b feature/footer
git add page.html
git commit -m "Add header to page"
git commit -m "Add footer to page"
git merge feature/header
git merge feature/footer
git tag -a v1.0 -m "First stable version with merged features"
git tag v1.0-test
git show v1.0
git show v1.0-test
git push origin v1.0
```

**Results/Output**:

Conflict and resolved conflits:
```
CONFLICT (add/add): Merge conflict in page.html
Automatic merge failed; fix conflicts and then commit the result.

Merge: a0e733d ae97a64
Author: alhambrx
Commit: Merge footer with resolved conflicts
```
Tags:
```
PS C:\Users\alham\source\repos\taller-master-ugr> git tag
v0.0.1
v1.0
PS C:\Users\alham\source\repos\taller-master-ugr> git show v1.0
tag v1.0
Tagger: alhambrx <alhambraespigares@gmail.com>
Date:   Fri Dec 26 23:14:47 2025 +0100

First stable version with merged features

commit a45e398810711c5fe338216ff3ccb37bca472e5f (HEAD -> intermediate, tag: v1.0)
Merge: a0e733d ae97a64
Author: alhambrx <alhambraespigares@gmail.com>
Date:   Fri Dec 26 23:14:34 2025 +0100

    Merge footer with resolved conflicts

diff --cc page.html
index bbaf76d,2fc99ff..1e26d0e
--- a/page.html
+++ b/page.html
@@@ -1,8 -1,8 +1,11 @@@
  <!DOCTYPE html>
  <html>
  <body>
 +  <header>
 +    <h1>Page.html</h1>
 +  </header>
+   <footer>
+     <p>footer</p>
+   </footer>
  </body>
  </html>

```

**Screenshots** 
### Conflict Markers Observed

```
<<<<<<< HEAD
  <header>
    <h1>Page.html</h1>
  </header>
=======
  <footer>
    <p>footer</p>
  </footer>
>>>>>>> feature/footer
```
This image shows the gitk of the merged commit
![Solved](image.png)

This graph shows both feature branches merging into the intermediate branch.
![Branch structure](image-1.png)
---

## 🎯 Key Learnings

**Main concepts I learned**:
1. How Git detects conflicts when the same file is added or modified in different branches.
2. How to manually resolve merge conflicts using conflict markers.
3. The difference between annotated and lightweight tags.

**Skills I improved**:
- Resolving merge conflicts safely
- Reading git log --graph and merge commits
- Using tags for versioning

---

## 🚧 Challenges Faced

### Challenge 1: Merge conflict
**Problem**: Both feature branches created page.html, which caused an add/add merge conflict when merging into the intermediate branch.

**Solution**: I opened the conflicted file, identified the conflict markers (<<<<<<<, =======, >>>>>>>), and manually merged both the header and footer content into a valid HTML structure. After verifying the result, I staged and committed the resolved file.

**Commands/Approach**:
```bash
git merge feature/footer
git add page.html
git commit -m "Merge footer with resolved conflicts"
```
---

## 💭 Personal Reflection

**What surprised me**:
I was surprised by how Git shows conflicting changes using conflict markers. Once understood, they make conflict resolution very systematic.
**What I found most difficult**:
Understanding the exact difference between annotated and lightweight tags took some experimentation, especially noticing the metadata stored in annotated tags.
**What I found most useful**:
Learning how to resolve merge conflicts.
**How I would apply this in real projects**:
In real projects, I would use feature branches for isolated development, carefully resolve conflicts during merges, and use annotated tags to mark stable releases. 

---

## 📊 Self-Assessment

Rate your confidence level for each topic (1-5, where 5 is very confident):

| Topic | Confidence (1-5) | Notes |
|-------|------------------|-------|
| Basic Git commands | 5 | Confortable |
| Branching & merging | 4 | Conofident after practice|
| Remote operations | 4 |Push and pull understood|
| Conflict resolution | 4 | Can resolve safely|
| History rewriting | 2 | Not covered|
| Git hooks | 1 | Not covered|
| Security practices | 2 | Basic|

---

## 🔗 Evidence/Artifacts

**Links to branches/commits**:
- Link to your outcome branch: `https://github.com/alhambrx/taller-master-ugr/tree/alh-outcomes/intermediate`
- Key commits:
  -a0e733d: Add header to page
  -ae97a64: Add footer to page
  -a45e398: Merge footer with resolved conflicts

**Additional files created** 
- page.html

---

## ✅ Completion Checklist

Before submitting, ensure you have:
- [x] Completed the exercise for your chosen level (including all parts)
- [x] Documented all commands used with their outputs
- [x] Described challenges and how you resolved them
- [x] Provided a thoughtful reflection on your learning
- [x] Self-assessed your confidence in each topic
- [x] Pushed your outcome branch to the remote repository
- [ ] Created a Pull Request (if required by your instructor)

---

## When to Use Each Tag Type

- **Annotated tags**: Used for production releases, versioned milestones, and when metadata (author, date, message) is important.
- **Lightweight tags**: Used for temporary testing, local references, or quick checkpoints.

Outputs comparison:
```
PS C:\Users\alham\source\repos\taller-master-ugr> git show v1.0
tag v1.0
Tagger: alhambrx <alhambraespigares@gmail.com>
Date:   Fri Dec 26 23:14:47 2025 +0100

First stable version with merged features

commit a45e398810711c5fe338216ff3ccb37bca472e5f (HEAD -> intermediate, tag: v1.0-test, tag: v1.0)
Merge: a0e733d ae97a64
Author: alhambrx <alhambraespigares@gmail.com>
Date:   Fri Dec 26 23:14:34 2025 +0100

    Merge footer with resolved conflicts

diff --cc page.html
index bbaf76d,2fc99ff..1e26d0e
--- a/page.html
+++ b/page.html
@@@ -1,8 -1,8 +1,11 @@@
  <!DOCTYPE html>
  <html>
  <body>
 +  <header>
 +    <h1>Page.html</h1>
 +  </header>
+   <footer>
+     <p>footer</p>
+   </footer>
  </body>
  </html>
PS C:\Users\alham\source\repos\taller-master-ugr> git show v1.0-test
commit a45e398810711c5fe338216ff3ccb37bca472e5f (HEAD -> intermediate, tag: v1.0-test, tag: v1.0)
Merge: a0e733d ae97a64
Author: alhambrx <alhambraespigares@gmail.com>
Date:   Fri Dec 26 23:14:34 2025 +0100

    Merge footer with resolved conflicts

diff --cc page.html
index bbaf76d,2fc99ff..1e26d0e
--- a/page.html
+++ b/page.html
@@@ -1,8 -1,8 +1,11 @@@
  <!DOCTYPE html>
  <html>
  <body>
 +  <header>
 +    <h1>Page.html</h1>
 +  </header>
+   <footer>
+     <p>footer</p>
+   </footer>
  </body>
  </html>
PS C:\Users\alham\
```

---

## 🧠 Reflection (Intermediate Level)

This exercise helped me understand how Git manages parallel development and why merge conflicts are a normal part of collaborative work. When I encountered my first merge conflict, I initially felt unsure because the file contained unfamiliar conflict markers. However, by carefully reading the `<<<<<<<`, `=======`, and `>>>>>>>` sections, I realized that Git was clearly showing the competing changes from each branch.

Resolving the conflict required deciding which parts of each branch should remain. In this case, the correct solution was to keep both the header and footer, combining them into a valid HTML structure. This taught me that conflict resolution is not about choosing one version blindly, but about understanding the intent behind each change.

I also learned the importance of tags in version control. Annotated tags are useful for marking official releases because they include metadata and messages, while lightweight tags are better for temporary references or testing. Unlike branches, tags do not move and represent fixed points in history.

Overall, this exercise increased my confidence using Git, and I think it will be especially useful when working in teams, managing releases, and maintaining a clean project history.

---

**Submission Date**: [26-12-2025]  
**Ready for Review**: ✅ Yes 
