---
title: Main Menu Camera Animation
description: "This page contains information about the main menu's camera animation."
authors: ["loren", "lucasc190"]
---

The main menu's camera animation is actually just one animation.

The animation is located in `art\frontend\scrooby\resource\pure3d\camset.p3d` and is titled `CAM_FE_Camera`.

The game hardcodedly plays certain frames of this animation when you select options on the menu.

This page documents which frames are used for what action.

| Start frame | End frame | Description           | Use                                |
|-------------|-----------|-----------------------|------------------------------------|
| 0           | 53        | Main To Newspaper     | New Game                           |
| 80          | 110       | Main To Couch         | Main To Options                    |
| 110         | 140       | Couch To Main         | Options To Main                    |
| 140         | 170       | Main To TV            | Resume Game                        |
| 200         | 230       | Main To VCR           | Main To Load Game                  |
| 230         | 260       | VCR To Main           | Load Game To Main                  |
| 320         | 350       | Main To Scrap Book    | Main To Scrap Book                 |
| 350         | 380       | Scrap Book To Main    | Scrap Book To Main                 |
| 530         | 560       | Couch To Controller   | Options To Controller              |
| 560         | 590       | Controller To Couch   | Controller To Options              |
| 600         | 630       | Couch To TV           | Options To View Credits            |
| 630         | 660       | TV To Couch           | View Credits To Options            |
| 660         | 690       | Couch To Krusty Thing | Options To Sound                   |
| 690         | 720       | Krusty Thing To Couch | Sound To Options                   |
| 721         | 770       | Animate In            | Start                              |
| 770         | 800       | Animate Out           | Unused                             |
| 810         | 830       | Scrap Book Open       | Scrap Book To Open Book/Game Stats |
| 830         | 850       | Scrap Book Close      | Open Book/Game Stats To Scrap Book |
| 880         | 913       | Main To Race Car      | Mini Game                          |
| 914         | 944       | Couch To Wasp         | Options To View Movies             |
| 944         | 974       | Wasp To Couch         | View Movies To Options             |
| 975         | 1005      | Wasp To TV            | View Movies To Play Movie          |
| 1005        | 1035      | TV To Wasp            | Play Movie To View Movies          |