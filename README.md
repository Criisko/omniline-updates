# omniline-updates

Where OmniLine (the build of openOMSI sold on Patreon) announces that a newer version exists.

The program reads `latest.json` here and downloads nothing: it tells the player which version is
out and opens the page it is sold from. That is why this file holds no address of an archive
anywhere. A copy of OmniLine that leaks onto a file-sharing site can be told that a newer
version exists, and can be sent to that page, but it cannot update itself.

## Editing this when a version is released

- `version`: the released version, exactly as the build reports it.
- `notes`: optional, one line, shown under the version in the launcher.
- `url`: required, the page the version is got from; it must start with `http://` or `https://`.
  Anything else is refused, so a tampered feed cannot open a file or run a program.

A file that does not answer, does not parse, or names an older version means no news, and is
never an error for the player.