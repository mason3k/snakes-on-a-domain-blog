---
title:  "Make it Easy to Do the Right Thing with WWBD"
date:   2022-12-22
categories: vscode venvs extensions
---

### The Problem

If you're like me, you know that even for small Python projects and scripts, you should be using a virtual environment. There are a gazillion reasons for this, most of which have been covered effectively elsewhere.

<!-- excerpt-end -->

This post is aimed at those of you who *know* you should be using venvs for your one-off apartment-hunt screenscraper/fantasy football stat aggregator/\*gasp\* real work script but don't because, let's face it, the typical venv workflow is not as simple as it could be (was that `/Scripts/Activate.ps1` or `scripts/activate.ps1`??).

![st-augustine]({{ "/assets/staugustine.jpeg" | relative_url }}){: .align-center}
*Lord, make me a good venv user, but not yet*
{: .text-center}

### WWBD to the Rescue

Lately, I've been living up to my venv ideals almost entirely due to a little [experimental VS Code extension called WWBD](https://visualstudiomagazine.com/articles/2022/06/10/wwbd.aspx) - What Would Brett Do?

Jesus, in this formulation, has been replaced by Python Jesus/Python core developer [Brett Cannon](https://fosstodon.org/@brettcannon
), who has spent quite a bit of time thinking about Python packaging, environment strategy, and developer best practices. He's now allowing us live a day (ok, fine, maybe just a second) in the life via this extension, which essentially automates venv creation, activation, and VS Code integration according to his virtual environment philosophy.

![ridealong]({{ "/assets/ridealong.webp" | relative_url }}){: .align-center}
*Kind of like a Python ride-along*
{: .text-center}

### The Caveats

Before people get grumpy, as people on the internet are wont to do, here are some caveats that the project itself is upfront about:

- The extension is experimental and may be swallowed by standard VS Code functionality someday
- The venv strategy is opinionated; if you are using for a large project or have complicated needs, you may want to take the extra 5 minutes to control/customize your own process instead of relying on this extension
- the selected Python interpreter must have venv and pip available/installed ([it has been included in Python binaries by default since Python 3.4](https://peps.python.org/pep-0453/))
- Only works when there is one clear workspace selected

### The Steps

1. Install the "WWBD" extension from the VS Code marketplace
1. To initiate a project, open the workspace, launch the Command Pallette, and type "WWBD: Create Environment"

That's it! Notice that a venv has been created, your workspace is using it to run code by default, and it is successfully added to your `.gitignore` so it's not being tracked by source control.

For more details on what's going on behind the scenes and why, you can refer to the [extension documentation/source code](https://github.com/brettcannon/WWBD) or [Brett's post on virtual environment strategy](https://python1233.rssing.com/chan-44877200/article12053.html), which I believe mirrors his approach in this extension pretty well.

### Hidden Gem

This is already pretty cool. But as an added bonus, if you already have a `requirements.txt` file in your workspace, those dependencies will automatically be installed into your new venv.

That means if you have been working on a project using your global Python interpreter before you saw the error of your ways, you can pipe `pip freeze` to a `requirements.txt` file and be all set to go in your new, enlightened life.

### Bonus

If you become rigid and dogmatic in your approach to venvs, as all good converts do, you can set the `PIP_REQUIRE_VIRTUALENV` environment variable to true; try to `pip install` after doing so will fail if a virtual environment is not activated.

No self-flagellation required.
