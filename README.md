# uwindsor.ca Submissions

This repository collects the project submissions from every group. Each group
submits its work by opening a **pull request** from its own fork.

## The one rule

**Fork this repository, push your work to a branch on your fork, and open a
pull request that names your group in the description.**

Do not try to push directly to this repository. It will not work, and the
section below explains why.

## Why you cannot push directly

- **The push is rejected.** Only the Aerrand team has write access, so
  `git push` to this repository fails with
  `Permission denied ... The requested URL returned error: 403`. This is
  expected and is not a problem with your account or your setup.
- **Write access would put every group's work at risk.** Anyone who can push
  here can also overwrite or delete `main` and any other group's branch, by
  accident or otherwise.
- **There is no record of who submitted what.** A direct push does not say
  which group it belongs to. A pull request shows the group, the author, the
  time, and every change in one place.
- **Nothing can be checked before it lands.** A pull request lets us catch
  problems such as committed API keys, `node_modules/`, or files in the wrong
  place, and leave feedback, before anything is added to the shared
  repository.

## Step-by-step

The example below is for **Group 6**. Replace `6` with your own group number.

### 1. Fork the repository

Open <https://github.com/errand-app-dev-team/uwindsor.ca.submittions> and click
**Fork** in the top right. This creates a copy under your own GitHub account
that you are allowed to push to.

Only **one member** of the group needs to fork. See
[Working with your teammates](#working-with-your-teammates) below.

### 2. Clone your fork

Replace `<your-username>` with the GitHub username that owns the fork:

```bash
git clone https://github.com/<your-username>/uwindsor.ca.submittions.git
cd uwindsor.ca.submittions
```

If you already cloned this repository before forking, you do not need to clone
again. Point your existing clone at your fork instead:

```bash
git remote set-url origin https://github.com/<your-username>/uwindsor.ca.submittions.git
```

### 3. Create your group's branch and switch to it

Git branch names cannot contain spaces, so write the group name with a hyphen:
lowercase `group`, a hyphen, and your group number.

| Your group | Your branch name |
|------------|------------------|
| Group 1    | `group-1`        |
| Group 6    | `group-6`        |
| Group 12   | `group-12`       |

```bash
git checkout -b group-6
```

### 4. Add your project files

Copy your project into the repository folder. Then stage and commit the files:

```bash
git add .
git commit -m "Group 6: initial submission"
```

### 5. Push your branch to your fork

```bash
git push -u origin group-6
```

### 6. Open the pull request

1. Open your fork on GitHub. Click the **Compare & pull request** button that
   appears after you push. If it does not appear, go to the **Pull requests**
   tab and click **New pull request**.
2. Check the two ends of the pull request:
   - **base repository:** `errand-app-dev-team/uwindsor.ca.submittions`,
     **base:** `main`
   - **head repository:** your fork, **compare:** `group-6`
3. Fill in the title and description as shown below.
4. Click **Create pull request**.

## What the pull request must contain

**The description must contain your group name.** A pull request without it
cannot be matched to a group and will not be counted as a submission.

Title:

```
Group 6 submission
```

Description:

```
Group: Group 6
Members: <full names of all group members>

Summary: <one or two sentences on what you are submitting>
```

## Updating your submission

Open **one** pull request per group. You do not need a new one for later
changes: anything you push to the same branch on your fork is added to the
open pull request automatically.

```bash
git add .
git commit -m "Describe what you changed"
git push
```

## Working with your teammates

One member forks the repository and opens the pull request. To let the rest of
the group push to that fork, the owner opens the fork on GitHub and goes to
**Settings → Collaborators → Add people**.

Teammates then clone the fork and check out the existing branch instead of
creating it again:

```bash
git clone https://github.com/<fork-owner-username>/uwindsor.ca.submittions.git
cd uwindsor.ca.submittions
git checkout group-6
git pull
```

## Do not

- Do **not** push to this repository directly. Push to your fork.
- Do **not** open more than one pull request per group.
- Do **not** use a branch name other than `group-<your number>`.
- Do **not** commit large binaries, `node_modules/`, virtual environments, build
  output, or secrets such as API keys. This repository is public, so anything
  you commit is visible to everyone. Add a `.gitignore` to your branch for
  these.

## Checklist before the deadline

- [ ] My branch is named `group-<number>` with my group's number.
- [ ] All of my group's code is committed and pushed to that branch on our fork.
- [ ] Our group has one open pull request into `main` of this repository.
- [ ] The pull request description contains our group name.
- [ ] I can see all of our files in the pull request's **Files changed** tab.

## Need help?

If you are not sure whether your submission went through, or you opened a pull
request by mistake, contact the course staff **before** the deadline.
