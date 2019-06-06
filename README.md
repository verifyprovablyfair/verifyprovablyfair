# sha256 & game outcome verification v0.1
<h3>sha256 verification</h3>

Example usage: https://verifyprovablyfair.github.io/verifyprovablyfair/?hash=ce57ecdcf1142238d61b57d2025457b2b0469bc5a17959e0193cdd0f495fbfc7&salt=34fd51a49d84e7257c1d07e889b3cb6432b917d7e4a0d3160d905287650a6841_2&srand=2&prand=2&randmax=4&outcome=4

If sha256(salt) is identical to hash provided then <b>Hash equals</b> will be displayed.
<br>Otherwise <b>Hash does not equal</b> will be displayed.

This script performs a sha256() function on the <i>salt</i> provided, and the compares the result with the claimed <i>hash</i> variable.<br>
If they're equal, <b>Hash equals</b> will be displayed.
<br>Otherwise <b>Hash does not equal</b> will be displayed.

<h3>Game outcome verification</h3>

Game outcome verification takes 4 arguments:<br>
srand (ServerRandom)<br>
prand (PlayerRandom)<br>
randmax (RandomNumberMax)<br>
outcome (<b>Claimed</b> Outcome)<br>

It performs the calculation of: (srand+prand)%(randmax+1) and compares it with the <i>Claimed outcome</i><br>
If it's equal then <b>Outcome equals</b> will be displayed.
<br>Otherwise <b>Outcome is NOT equal!</b> will be displayed.

If both sha256 verification and outcome verification passed then the message <b>Your game was provably-fair</b> is displayed. Otherwise it displays <b>Your game was unfair</b>
