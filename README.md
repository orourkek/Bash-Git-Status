Bash-Git-Status
===============

This is my BASH command line configuration, which adds Git repo status information to the BASH command line (amongst other things). The information displayed is:

1. Repo name (will use remote origin if available)
2. Current branch name
3. Status (via colors & symbols)

In the following format:

    $color$repo_name ($branch_name) $indicator

The repo status will be displayed as follows:

* Uncommitted Changes (dirty working directory) - Yellow text with indicator "*"
* Ahead of Origin - Yellow text with indicator "✘"
* Up to date - Green text with indicator "✓"

**This configuration also defines PS1 as follows:**

Inside Git repo:

    "$WHITEBOLD[$BLACKBOLD\u $WHITEBOLD\t $(git-info) $WHITEBOLD] $ $NO_COLOUR"

Not in Git repo:

    "$WHITEBOLD[$BLACKBOLD\u $WHITEBOLD\t $RED\w$WHITEBOLD] $WHITEBOLD$ $NO_COLOUR"
