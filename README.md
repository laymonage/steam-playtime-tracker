# steam-playtime-tracker

Track your Steam library playtime with git.

To use this repository with your Steam account, click on "Use this template"
and "Create a new repository". Then, go to the repository's "Settings >
Actions > General > Workflow permissions" and enable "Read and write
permissions". Finally, go to "Settings > Secrets and Variables > Actions" and
add the following:

- `STEAM_WEB_API_KEY` as a Secret. You can get this from https://steamcommunity.com/dev/apikey.
- `STEAM_ID` as a Variable. You can get this from https://api.steampowered.com/ISteamUser/ResolveVanityURL/v1/?key=$STEAM_WEB_API_KEY&vanityurl=yourvanityurlusername.

The workflow is run every day to update the data, but you can trigger it
[manually][manual-workflow] or by pushing a new commit to the repository. The
data can then be found inside the `data.json` file on the `data` branch.

[manual-workflow]: https://docs.github.com/en/actions/managing-workflow-runs/manually-running-a-workflow
