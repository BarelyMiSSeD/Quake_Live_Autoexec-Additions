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
<b>If you leave it undedited it will use the . key to cycle through the brightnesses</b><br>
seta r_gamma "1.4"<br>
bind . "vstr brightness"<br>
set brightness "vstr upbright1"<br>
set upbright1 "seta r_gamma 1.0; set brightness vstr upbright2"<br>
set upbright2 "seta r_gamma 1.2; set brightness vstr upbright3"<br>
set upbright3 "seta r_gamma 1.4; set brightness vstr upbright4"<br>
set upbright4 "seta r_gamma 1.6; set brightness vstr upbright5"<br>
set upbright5 "seta r_gamma 1.8; set brightness vstr dnbright6"<br>
set dnbright6 "seta r_gamma 2.0; set brightness vstr upbright1"<br>
<br><br>
# CA/Wipeout config switch Menu to callvote Shufffle, exec ca config, exec wipeout config
<b>If you leave it undedited it will use the arrow keys (left and right) to cycle through the menus, and down to execute the selection. change the 'ca' and 'wipeout', after the exec commands, to whatever your .cfg files are named.</b><br>
bind LEFTARROW "vstr sm_prev"<br>
bind RIGHTARROW "vstr sm_next"<br>
bind DOWNARROW "vstr sm_action"<br>
set sm_prev vstr sm_menu03<br>
set sm_next vstr sm_menu01<br>
set sm_action "callvote shuffle"<br>
set sm_menu01 "set sm_next vstr sm_menu02; set sm_prev vstr sm_menu03; print ^7:[ ^1Shuffle^7 ExecCA ExecWipeout ]::; set sm_action callvote shuffle"<br>
set sm_menu02 "set sm_next vstr sm_menu03; set sm_prev vstr sm_menu01; print ^7:[ Shuffle ^1ExecCA^7 ExecWipeout ]::; set sm_action vstr ca"<br>
set sm_menu03 "set sm_next vstr sm_menu01; set sm_prev vstr sm_menu02; print ^7:[ Shuffle ExecCA ^1ExecWipeout^7 ]::; set sm_action vstr wipeout"<br>
set ca "bind MWHEELDOWN weapprev"<br>
set wipeout "bind MOUSE3 +button2;bind MWHEELDOWN say !power"<br>
<br><br>
# Wipeout Easy Key<br>
<b>You can bind a key to these actions and not need to bind the 'say !power' command, for use in most games. Though you may want it for a way to change your power-up. Your choice.<br>
The key, 'q' here, will execute the !power command, pause, use item, unuse item, and execute !power again.<br>
Since the QL Wipeout game starts you with the power-up, this key will switch to the med-kit, use it, and switch back to the power-up.</b><br>
bind q "say !power;wait 50;+button2;-button2;say !power"<br>
