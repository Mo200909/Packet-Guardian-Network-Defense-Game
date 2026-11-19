# Packet Guardian

> **AI-generated code.** This browser game was vibe-coded with Claude Opus 5.5 (Anthropic). I designed the game and directed every change; the code itself is AI-generated. Below is how to play it and where it simplifies reality.

A tower defense game where you protect a hospital's network. Infected packets travel from the Internet toward the hospital's files, and you build security tools to stop them. It is styled as a 90s desktop that gets taken over by Matrix-style code as you lose.

**Or run it locally:** download the `.html` file from this repo and open it in any modern browser. No install or server needed.

## How to play

- Click the canvas to start. Sound starts on that first click.
- Pick a tower with the buttons or keys **1-4**, then click empty desktop space to place it.
- Click a placed tower to upgrade it (up to level 3) or sell it.
- Click a packet to destroy it by hand. Destroying a good packet is a false positive and costs points.
- Click a folder on the left to open that file and see how damaged it is.
- **Space** starts the next wave. **F** toggles 2x speed. **Esc** closes windows.
- Survive 6 waves. You lose when all three files (patient records, lab results, pharmacy) are corrupted.

## What each tool models

| In the game | Real-world idea | Simplification |
|---|---|---|
| Firewall | Blocks traffic by port (Telnet 23, SMB 445, RDP 3389) | Real firewalls use full rule sets, not three ports |
| Filter | Deep packet inspection; finds malware on normal ports and opens encrypted tunnels | Real TLS inspection needs certificates and has privacy trade-offs |
| Rate limiter | Slows traffic and drops excess during a DDoS | Real DDoS defense usually happens upstream (ISP or scrubbing service) |
| Honeypot | A decoy that attracts attackers | Real honeypots mainly gather intelligence; they don't remove attacks from the network |
| Backup server | Offline backups as a ransomware recovery plan | Restore time is shortened to 5 seconds |
| Email filter | Attachment scanning | Real filters use many signals, not just the file extension |
| SIEM | Central alert log and monitoring | Real SIEMs don't predict the next attack; the forecast is a game mechanic |

## Attacks

- **Infected packets** on dangerous ports, plus **disguised** packets that look like normal HTTPS or HL7 traffic.
- **Encrypted tunnels** that split into hidden bad packets when opened.
- **DDoS floods** (waves 3 and 5): many small packets that overload the network and slow every tower.
- **Ransomware** (waves 4 and 6): if it gets through, you choose to pay (you can go into debt), restore from backup if you bought one, or refuse and shut down.
- **Easter egg:** a nod to the ILOVEYOU worm (May 2000), which hid its `.vbs` extension so it looked like a text file.

## Not real statistics

The odds in the game are balance choices, not measured data:
- Paying the ransom fails 40% of the time.
- Restoring from backup fails 25% of the time.

The real lesson they point to is that neither paying nor restoring is guaranteed.

## Inspiration and assets

The tower-defense mechanics (economy, upgrades, slowing towers, layered and boss enemies) are inspired by the tower-defense genre in general. No code, art, or sound from any other game is included. All visuals are drawn in code, and all sound is generated in the browser.
