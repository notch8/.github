# notch8/.github

Organization-wide GitHub configuration: shared issue templates under `.github/ISSUE_TEMPLATE`, the
public org profile under `profile/`, and scheduled automation that belongs to no single project.

## Roll sprint

`.github/workflows/roll_sprint.yml` runs every Monday at 6am Pacific and moves every Team Violet
Board 2.0 item from the previous sprint into the current one, except items in Done. It covers every
repository on the board. It needs the `VIOLET_BOARD_TOKEN` repository secret: a classic personal
access token with the `project` and `read:org` scopes, kept in 1Password. Run it by hand from the
Actions tab; the `dry_run` input lists what would move without changing the board.
