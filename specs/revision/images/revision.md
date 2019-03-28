# Revision

--

# Main goals by role

## Author of Revision (how?)

- defend approach
- get revision merged in
- update revision based on feedback
- reply to & resolve discussion
- Help reviewers accept revision

## Reviewer of Revision (how?)

- Review code to be merged in
- Discuss any changes that don't make sense
- propose concrete suggestions
- Accept all changes = accept revision

## Viewer of Revision

- Get insight into revision
- Help discussions along

## Owner of repository (what?)

- Repository health
- Bigger picture

--

# Jobs to be done by role

## All three

- start a discussion on 1 specific line
- start a discussion on a file
- start a discussion on the revision
- reply to a discussion

## Author of Revision

- Update revision with new commits
- Resolve a discussion
- Accept/reject a suggestion
- split/join hunks
- See review submissions
  - Accepted review ( accepted hunks )
  - Request changes ( accepted hunks + open discussions )
  - Comment ( accepted hunks + open discussions )

## Reviewer of Revision

- split/join hunks
- Resolve discussion
- Start discussion on hunks
- accept hunks
- Make suggestions

## Owner of repository

- close revision

--

# Questions

## Review process

- do we want to review hunks or commits? List pros & cons
  - can we do both? Review revision by commits / by hunks
  - Can we help users be better at the structured commits flow vs Hunks/brain approach?

## splitting of hunks

- how do hunks get split initially
- do we need to join hunks
- if I, a reviewer, split a hunk, do other reviewers need to review those hunks seperately as well
- do we need to alert the review author of this

## Revision author role

- what does the author need to keep track of to keep the reviews going?
  - starting of discussions
  - replies to discussions
  - resolvement of discussions
  - Acceptance of hunks
  - Splitting / joining of hunks
  - pushing of updates
-

--

# GUI Elements

## Timeline

- new commit
- role assignment
- comment on revision
  - reply to comment
- Suggestion on revision
  - Acceptance of suggestion
  - rejection of suggestion
  - comment on suggestion
- Acceptance of revision
- Requesting changes
  - discussion on hunks
    - reply to discussion
    - resolution of discussion
- Rejection of revision
- Merge of revision
-

## Reviewer page

- overview
  - total hunks
  - hunks reviewed
  - hunks in discussion
    - open
    - resolved
  - hunks to be review
- Since last review/checkin
  - # of new hunks
  - new replies to discussion
  - resolved discussions
