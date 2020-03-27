# Quake_Live_Autoexec-Additions

Here are some additions that I use in my autoexec.cfg for different things.
<br>
# Muting/UnMuting in game voice chat
<b>If you leave it undedited it will use the end key to toggle the in game voice and print to the console</b><br>
bind end "vstr voice"<br>
set voice vstr voiceoff<br>
set voiceoff "set voice vstr voiceon; seta s_voicevolume 0.00; print Voice Chat Off"<br>
set voiceon "set voice vstr voiceoff; seta s_voicevolume 1; print Voice Chat On"<br>
<br><br>
# Changing Enemy Force Colors
<b>If you leave it undedited it will use the n key to toggle the forced enemy colors and print the color</b><br>
bind n "vstr enemycolor"<br>
set enemycolor "vstr greencolor"<br>
set greencolor "seta cg_enemyUpperColor 0x00FF00FF; seta cg_enemyLowerColor 0x00FF00FF; seta cg_enemyHeadColor 0x00FF00FF; set enemycolor vstr bluecolor; print ^2Green Enemies"<br>
set bluecolor "seta cg_enemyUpperColor 0x00BFFFFF; seta cg_enemyLowerColor 0x00BFFFFF; seta cg_enemyHeadColor 0x00BFFFFF; set enemycolor vstr yellowcolor; print ^4Blue Enemies"<br>
set yellowcolor "seta cg_enemyUpperColor 0xff8000ff; seta cg_enemyLowerColor 0xff8000ff; seta cg_enemyHeadColor 0xff8000ff; set enemycolor vstr redcolor; print ^3Yellow Enemies"<br>
set redcolor "seta cg_enemyUpperColor 0xFF000088; seta cg_enemyLowerColor 0xFF000088; seta cg_enemyHeadColor 0xFF000088; set enemycolor vstr purplecolor; print ^1Red Enemies"<br>
set purplecolor "seta cg_enemyUpperColor 0xFF00FFFF; seta cg_enemyLowerColor 0xFF00FFFF; seta cg_enemyHeadColor 0xFF00FFFF; set enemycolor vstr whitecolor; print ^6Purple Enemies"<br>
set whitecolor "seta cg_enemyUpperColor 0xFFFFFF88; seta cg_enemyLowerColor 0xFFFFFF88; seta cg_enemyHeadColor 0xFFFFFF88; set enemycolor vstr greencolor; print ^7White Enemies"<br>
<br><br>
# Cycling through map brigtness settings
<b>If you leave it undedited it will use the . key to cycle through the brightnesses</b>
seta r_gamma "1.4"<br>
bind . "vstr brightness"<br>
set brightness "vstr upbright1"<br>
set upbright1 "seta r_gamma 1.0; set brightness vstr upbright2"<br>
set upbright2 "seta r_gamma 1.2; set brightness vstr upbright3"<br>
set upbright3 "seta r_gamma 1.4; set brightness vstr upbright4"<br>
set upbright4 "seta r_gamma 1.6; set brightness vstr upbright5"<br>
set upbright5 "seta r_gamma 1.8; set brightness vstr dnbright6"<br>
set dnbright6 "seta r_gamma 2.0; set brightness vstr upbright1"<br>
