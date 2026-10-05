# Tripothon S1 submission folder

Everything about the hackathon lives here and nowhere else in the repository.
Pedro's ask (2026-10-04): "make everything related to the hackathon in a folder
separated, and scrape the site, check if the project is in conformity with the
hackathon, and make it ready for it."

**Deadline: October 5, 23:59 AoE (UTC-12), which is October 6 08:59 in Brasilia (hard).**
Submission portal: https://activity.tripo3d.ai/en/submit (sign in with the Tripo account).

| File | What it is |
|---|---|
| HANDBOOK.md | The handbook (Feishu, September 30) and the official site, captured in full |
| CONFORMITY.md | Every rule against the project: what passes, what is open, who does it |
| SUBMISSION.md | The texts for the form, the secondary-development declaration, the three decisions Pedro owns, the checklist |
| VIDEO_SCRIPT.md | The 1 to 2 minute walkthrough: shot list, voiceover, recording checklist |
| TRIPO_USAGE.md | The tool-track evidence: pipeline, shipped assets, generation batches |
| board/ | The visual asset board: world and HUD stills (1600 x 900 and 1920 x 1080 JPG) and building turntables (GIF) |
| increment-commits.txt | Every commit since the submission window opened (the "work increment" judges score) |

## State on 2026-10-04

Done by the agent: the handbook and site captured; the conformity check; the
submission texts; the asset board; the Tripo evidence; build 37 (the adjusted balance
patch, the plaza fix, the faction card) with the server redeployed.

Pedro's part, in order:

1. The source repository stays private (Pedro's rule). The playable builds live in the
   releases-only public repository https://github.com/pedrohsmaia/four-thrones-releases (release
   v0.1.0-build37). Check the download link in a private browser window before submitting.
2. Register ("Start Building" on the event page), then open the portal
   https://activity.tripo3d.ai/en/submit, sign in, pick Games and the Tripo tool track.
3. Test the macOS build once (unzip, `xattr -cr FourThrones.app`), or ship Windows only.
4. Record the walkthrough (VIDEO_SCRIPT.md), upload, paste the link.
5. Fill the form with SUBMISSION.md; attach or link the board.
6. Optional: one build-log post with #Tripothon and @tripoai.

Decided on 2026-10-04: the gift line ("A gift for RTS and auto-battler fans"), no title-screen
dedication, hosting on a GitHub release.
