# TASK-01 — Create & Resolve a Merge Conflict

## Objective
To understand how merge conflicts happen and how to correctly resolve them in real open-source workflows.

---

## Setup

Create a folder with your **GitHub Username** inside the `task-01` folder.  
Inside your `GithubId` folder, create a file named **data.txt** with the following content:

```
OpenCode FOSS Wing – Merge Conflict Task

Line 1: Learning real-world Git workflows.
Line 2: This line will be modified differently in two branches.
Line 3: Git conflicts are normal in open source.
Line 4: I am learning how to resolve them properly.
```

---

## Steps To Solve

### 1. Create two branches

```bash
git checkout -b foss-task01-a
```
Edit Line 2 to:
```
This line is modified in Branch A.
```
Commit:
```bash
git commit -am "Branch A change"
```

```bash
git checkout -b foss-task01-b
```
Edit Line 2 to:
```
This line is modified in Branch B.
```
Commit:
```bash
git commit -am "Branch B change"
```

---

### 2. Create the conflict

```bash
git checkout foss-task01-a
git merge foss-task01-b
```

---

### 3. Resolve the conflict

Resolve Line 2 to:

```
This line is modified in Branch A and Branch B.
```

Then commit:

```bash
git add data.txt
git commit -m "Resolved merge conflict in data.txt"
```

---

## Mandatory PR Requirement

Run:
```bash
git log --oneline --graph --all
```

Take a screenshot and attach it in your **Pull Request description**.

---

## PR Submission

- `data.txt` exists  
- Conflict is resolved correctly  
- Screenshot attached  
- Commit history shows both branches and merge commit  

## Answer the following question in your own Language in PR Description
1. What was the differnece between `git commit -m "..."` and `git commit -am "..."`.
2. What was the main cause for the merge conflict according to you?
