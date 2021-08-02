<template>
  <div>
    <Navbar/>
    <div class="container">
      <div class="breadcrumb">
        <NuxtLink to="/">GOD</NuxtLink> &raquo;
        <NuxtLink to="/">Castlevania: Symphony of the Night</NuxtLink> &raquo;
        System
      </div>
      <Header/>
      <h2>System</h2>
      <hr/>
      <main>
        <p>Here I pretend to explain how the game works. But it's still in progress...</p>
        <p>Your objective in the game is to find out why did the Castle appeared and to destroy it. In the process, you'll find various types of enemies between animals, undead, demons, ghosts and beasts. When you defeat an enemy, you get <abbr title="Experience Points">EXP</abbr> and it may drop items like 'Hearts' (necessary to use sub-weapons), GOLD (used at the Master Librarian shop to buy items) or a rare item which may be GOLD, a sub-weapon, a equipment or a [use] item (that can be used only once).</p>
        <p>Accumulating a specific amount of <abbr title="Experience Points">EXP</abbr>, Alucard gains a Level. When it happens, his attributes grow and Alucard gets more powerful.</p>
        <a id="Attributes"></a><h3>Attributes</h3>
        <table>
          <tr><td valign="top"><b>LV:</b></td><td>(Level) Represents the evolution level of the character. Attribute which best represents his power.</td></tr>
          <tr><td height="18"></td></tr>
          <tr><td valign="top"><b>HP:</b></td><td>(Hit Points/Health Power) It's the vital energy, represents the amount of damage the character can withstand. The damage taken is deducted from <abbr title="Health Points">HP</abbr>. It may be restored using items, spells or entering a 'Save Orb'. When the character gets much damage and his <abbr title="Health Points">HP</abbr> reaches zero, he dies.</td></tr>
          <tr><td height="18"></td></tr>
          <tr><td valign="top"><b>MP:</b></td><td>(Magic Points/Mind Power) It's the mental energy. Necessary to use spells. Each spell requires a specific amount of <abbr title="Magic Points">MP</abbr> to be realized. For each executed spell, its respective amount of <abbr title="Magic Points">MP</abbr> is deducted. After consumed, <abbr title="Magic Points">MP</abbr> slowly regenerates within time or may be instantly restored using a <Item item="Manna prism"/> or entering a 'Save Orb'. When Alucard's <abbr title="Magic Points">MP</abbr> is completely restored, a blue aura is emitted from his body. If Alucard don't have enough <abbr title="Magic Points">MP</abbr> for a spell, it can't be executed.</td></tr>
          <tr><td height="18"></td></tr>
          <tr><td valign="top"><b>STR:</b></td><td>(Strength) It's added to the <abbr title="Attack">ATT</abbr> of weapons to calculate the damage done by Physical attacks. When Alucard is unarmed, the damage done by his attack is equal the difference between his <abbr title="Strength">STR</abbr> and enemy's <abbr title="Defense">DEF</abbr>.</td></tr>
          <tr><td height="18"></td></tr>
          <tr><td valign="top"><b>CON:</b></td><td>(Constitution) The character's resistance. Determines the defense and the effect time of curses and poisoning. The amount of <abbr title="Defense">DEF</abbr> is influenciated by this attribute.</td></tr>
          <tr><td height="18"></td></tr>
          <tr><td valign="top"><b>INT:</b></td><td>(intelligence) Determines the damage inflicted by  spells and 'Sub-Weapons'.</td></tr>
          <tr><td height="18"></td></tr>
          <tr><td valign="top"><b>LCK:</b></td><td>(Luck) Determines the chances to find items and realize 'Critical Attacks', which when occur, causes double damage.</td></tr>
          <tr><td height="18"></td></tr>
          <tr><td valign="top"><b>ATT:</b></td><td>(Attack) Determines the damage an attack can cause. An attack with a weapon is equal the weapon's <abbr title="Attack">ATT</abbr> added to the character <abbr title="Strength">STR</abbr> and some <abbr title="Attack">ATT</abbr> bonus from other equipment.</td></tr>
          <tr><td height="18"></td></tr>
          <tr><td valign="top"><b>DEF:</b></td><td>(Defense) Represents the ability to resist damage. Each <abbr title="Defense">DEF</abbr> point nulls one enemy's <abbr title="Attack">ATT</abbr> point. Is equal the sum of the <abbr title="Defense">DEF</abbr> of all armors and <abbr title="Defense">DEF</abbr> bonus given by <abbr title="Constitution">CON</abbr>.</td></tr>
        </table>
        <a id="Menu-Screen"></a><h3>Menu Screen</h3>
        <p>This picture is from Alucard's status screen'. It shows his condition and attributes.<br/>
        Point to the fields to view its description.</p>
        <map id="map" name="map">
          <area title="Character Picture." shape="poly" coords="34,26,156,26,156,190,136,190,136,212,110,212,110,190,64,190,64,212,34,212" alt=""/>
          <area title="Character Name." shape="rect" coords="256,32,362,44" alt=""/>
          <area title="Level: Represents the evolution level of the character. Attribute which best represents his power." shape="rect" coords="498,32,572,44" alt=""/>
          <area title="Actual Level: Represents the actual evolution level of the character." shape="rect" coords="594,32,620,44" alt=""/>
          <area title="HP (Hit Points/Health Power): It's the vital energy, represents the amount of damage the character can withstand. When the character get much damage and his HP reaches zero, he dies." shape="rect" coords="192,64,218,76" alt=""/>
          <area title="Current HP: Represents the current amount of HP the character have." shape="rect" coords="288,64,346,76" alt=""/>
          <area title="Max HP: Represents the maximum amount of HP the character can have." shape="rect" coords="370,64,428,76" alt=""/>
          <area title="Status: Inform the current condition the character is like: 'Poison', 'Stone', 'Curse' etc." shape="poly" coords="498,64,588,64,588,76,580,76,580,100,522,100,522,76,498,76" alt=""/>
          <area title="MP (Magic Points/Mind Power): It's the mental energy. Necessary to use spells. Each spell requires a specific amount of MP to be executed." shape="rect" coords="192,88,218,100" alt=""/>
          <area title="Current MP: Represents the current amount of MP the character have." shape="rect" coords="304,88,346,100" alt=""/>
          <area title="Max MP: Represents the maximum amount of HP the character can have." shape="rect" coords="386,88,428,100" alt=""/>
          <area title="Hearts: Necessary to use 'Sub-Weapons' like 'Dagger', 'Axe', 'Holy-water', etc. Each 'Sub-Weapon' requires a specific amount of 'Hearts' to be used." shape="rect" coords="192,112,266,124" alt=""/>
          <area title="Current Hearts: Represents the current amount of 'Hearts' the character have." shape="rect" coords="304,112,346,124" alt=""/>
          <area title="Max Hearts: Represents the maximum amount of HP the character can have." shape="rect" coords="386,112,428,124" alt=""/>
          <area title="STR (Strength): Added to ATT to calculate damage done by physical attacks." shape="rect" coords="66,192,108,204" alt=""/>
          <area title="Base STR: Informs the strength (and the ATT) of the character without equipment." shape="rect" coords="138,192,164,204" alt=""/>
          <area title="STR Bonus: Informs the strength bonus from equipment and relics." shape="rect" coords="184,192,210,204" alt=""/>
          <area title="CON (Constitution): The character's resistance. Determines the defense and the effect time of curses and poisoning." shape="rect" coords="66,216,108,228" alt=""/>
          <area title="Base CON: Informs the constitution of the character without equipment." shape="rect" coords="138,216,164,228" alt=""/>
          <area title="CON Bonus: Informs the constitution bonus from equipment and relics." shape="rect" coords="184,216,210,228" alt=""/>
          <area title="INT (intelligence): Determines the damage inflicted by  spells and 'Sub-Weapons'." shape="rect" coords="66,240,108,252" alt=""/>
          <area title="Base INT: Informs the intelligence of the character without equipment." shape="rect" coords="138,240,164,252" alt=""/>
          <area title="INT Bonus: Informs the intelligence bonus from equipment and relics." shape="rect" coords="184,240,210,252" alt=""/>
          <area title="LCK (Luck): Determines the chances to find items and realize 'Critical Attacks'." shape="rect" coords="66,264,108,276" alt=""/>
          <area title="Base LCK: Informs the luck of the character without equipment." shape="rect" coords="138,264,164,276" alt=""/>
          <area title="LCK Bonus: Informs the luck bonus from equipment and relics." shape="rect" coords="184,264,210,276" alt=""/>
          <area title="EXP (Experience): Acumulating a specific amount of EXP, Alucard gains a level. When it happens, your attributes grow and Alucard gets more powerful." shape="rect" coords="66,304,108,316" alt=""/>
          <area title="Current EXP: The current battle experience the character have." shape="rect" coords="208,304,298,316" alt=""/>
          <area title="Next: The amount of EXP necessary to reach the next level." shape="rect" coords="66,328,124,340" alt=""/>
          <area title="Current Next: The current amount of EXP necessary to reach the next level.." shape="rect" coords="288,328,298,340" alt=""/>
          <area title="Gold: Symphony of the Night currency. Necessary to buy items at Librarian's Shop." shape="rect" coords="66,352,124,364" alt=""/>
          <area title="Current Gold: Informs the current amount of Gold the character have." shape="rect" coords="208,352,298,364" alt=""/>
          <area title="ATT (Attack): Determines the damage a attack can cause." shape="rect" coords="498,130,562,154" alt=""/>
          <area title="Right ATT: Informs the damage the right hand attack causes." shape="rect" coords="618,128,660,140" alt=""/>
          <area title="Left ATT: Informs the damage the left hand attack causes." shape="rect" coords="618,148,660,160" alt=""/>
          <area title="DEF (Defense): Represents the ability to resist damage. Each DEF point nulls one enemy's ATT point." shape="rect" coords="498,170,562,194" alt=""/>
          <area title="Current DEF: Informs the current amount of defense the character have." shape="rect" coords="618,180,660,192" alt=""/>
          <area title="Rooms: The number of &quot;screens&quot; visited in within the Castle." shape="rect" coords="482,252,556,264" alt=""/>
          <area title="Current Rooms: Informs the current amount of &quot;screens&quot; visited in within the Castle." shape="rect" coords="610,252,668,264" alt=""/>
          <area title="Kills: Number of enemies killed." shape="rect" coords="482,280,546,292" alt=""/>
          <area title="Current Kills: Informs the current number of enemies killed." shape="rect" coords="578,280,668,292" alt=""/>
          <area title="Time: Game Time." shape="rect" coords="420,336,476,348" alt=""/>
          <area title="Current Time: Informs the current Game Time." shape="rect" coords="514,336,636,348" alt=""/>
        </map>
        <center><img src="~static/img/menu.gif" width="720" alt="Menu Screen" usemap="#map"/></center>
        <p>When Alucard gains a level, some of his attributes growth randomly. <abbr title="Strength">STR</abbr>, <abbr title="Constitution">CON</abbr>, <abbr title="Intelligence">INT</abbr> and <abbr title="Luck">LCK</abbr>, can rise by 0, 1 or 2 points, however, if one of them rises 2, the others will rise 0. The other attribute that grows randomly is the <abbr title="Magic Points">MP</abbr> which rises 4 or 5 points. So the best results for a level up are <abbr title="Strength">STR</abbr>, <abbr title="Constitution">CON</abbr>, <abbr title="Intelligence">INT</abbr> and <abbr title="Luck">LCK</abbr> to rise 1 point and <abbr title="Magic Points">MP</abbr> to rise by 5. Hearts always rises 2 and <abbr title="Health Points">HP</abbr> rises as described in the next table along with the amount of <abbr title="Experience Points">EXP</abbr> necessary to reach each level.</p>
        <table style="width: 310px">
          <tr><td width="35">LV</td><td width="90">EXP</td><td width="90">Next</td><td>HP Bonus</td></tr>
        </table>
        <div style="width: 310px; height: 90px; margin: 0 auto; overflow: auto">
          <table style="width: 293px">
            <tr><td width="35">01</td><td width="90">0</td><td width="90">100</td><td>0</td></tr>
            <tr><td>02</td><td>100</td><td>150</td><td>1</td></tr>
            <tr><td>03</td><td>250</td><td>200</td><td>1</td></tr>
            <tr><td>04</td><td>450</td><td>250</td><td>1</td></tr>
            <tr><td>05</td><td>700</td><td>300</td><td>1</td></tr>
            <tr><td>06</td><td>1000</td><td>350</td><td>1</td></tr>
            <tr><td>07</td><td>1350</td><td>400</td><td>1</td></tr>
            <tr><td>08</td><td>1750</td><td>450</td><td>1</td></tr>
            <tr><td>09</td><td>2200</td><td>500</td><td>1</td></tr>
            <tr><td>10</td><td>2700</td><td>550</td><td>3</td></tr>
            <tr><td>11</td><td>3250</td><td>600</td><td>3</td></tr>
            <tr><td>12</td><td>3850</td><td>650</td><td>3</td></tr>
            <tr><td>13</td><td>4500</td><td>700</td><td>3</td></tr>
            <tr><td>14</td><td>5200</td><td>750</td><td>3</td></tr>
            <tr><td>15</td><td>5950</td><td>800</td><td>3</td></tr>
            <tr><td>16</td><td>6750</td><td>850</td><td>3</td></tr>
            <tr><td>17</td><td>7600</td><td>900</td><td>3</td></tr>
            <tr><td>18</td><td>8500</td><td>950</td><td>3</td></tr>
            <tr><td>19</td><td>9450</td><td>1000</td><td>3</td></tr>
            <tr><td>20</td><td>10450</td><td>1250</td><td>6</td></tr>
            <tr><td>21</td><td>11700</td><td>1500</td><td>6</td></tr>
            <tr><td>22</td><td>13200</td><td>1900</td><td>6</td></tr>
            <tr><td>23</td><td>15100</td><td>2400</td><td>6</td></tr>
            <tr><td>24</td><td>17500</td><td>2900</td><td>6</td></tr>
            <tr><td>25</td><td>20400</td><td>3300</td><td>6</td></tr>
            <tr><td>26</td><td>23700</td><td>3500</td><td>6</td></tr>
            <tr><td>27</td><td>27200</td><td>3700</td><td>6</td></tr>
            <tr><td>28</td><td>30900</td><td>4100</td><td>6</td></tr>
            <tr><td>29</td><td>35000</td><td>4500</td><td>6</td></tr>
            <tr><td>30</td><td>39500</td><td>5000</td><td>10</td></tr>
            <tr><td>31</td><td>44500</td><td>5500</td><td>10</td></tr>
            <tr><td>32</td><td>50000</td><td>6000</td><td>10</td></tr>
            <tr><td>33</td><td>56000</td><td>5500</td><td>10</td></tr>
            <tr><td>34</td><td>61500</td><td>7000</td><td>10</td></tr>
            <tr><td>35</td><td>68500</td><td>7500</td><td>10</td></tr>
            <tr><td>36</td><td>76000</td><td>8000</td><td>10</td></tr>
            <tr><td>37</td><td>84000</td><td>8500</td><td>10</td></tr>
            <tr><td>38</td><td>92500</td><td>9000</td><td>10</td></tr>
            <tr><td>39</td><td>101500</td><td>8500</td><td>10</td></tr>
            <tr><td>40</td><td>110000</td><td>10000</td><td>20</td></tr>
            <tr><td>41</td><td>120000</td><td>10000</td><td>20</td></tr>
            <tr><td>42</td><td>130000</td><td>10000</td><td>20</td></tr>
            <tr><td>43</td><td>140000</td><td>10000</td><td>20</td></tr>
            <tr><td>44</td><td>150000</td><td>10000</td><td>20</td></tr>
            <tr><td>45</td><td>160000</td><td>10000</td><td>20</td></tr>
            <tr><td>46</td><td>170000</td><td>10000</td><td>20</td></tr>
            <tr><td>47</td><td>180000</td><td>10000</td><td>20</td></tr>
            <tr><td>48</td><td>190000</td><td>10000</td><td>20</td></tr>
            <tr><td>49</td><td>200000</td><td>10000</td><td>20</td></tr>
            <tr><td>50</td><td>210000</td><td>12000</td><td>30</td></tr>
            <tr><td>51</td><td>222000</td><td>12000</td><td>30</td></tr>
            <tr><td>52</td><td>234000</td><td>12000</td><td>30</td></tr>
            <tr><td>53</td><td>246000</td><td>12000</td><td>30</td></tr>
            <tr><td>54</td><td>258000</td><td>12000</td><td>30</td></tr>
            <tr><td>55</td><td>270000</td><td>12000</td><td>30</td></tr>
            <tr><td>56</td><td>282000</td><td>12000</td><td>30</td></tr>
            <tr><td>57</td><td>294000</td><td>12000</td><td>30</td></tr>
            <tr><td>58</td><td>306000</td><td>12000</td><td>30</td></tr>
            <tr><td>59</td><td>318000</td><td>12000</td><td>30</td></tr>
            <tr><td>60</td><td>330000</td><td>14000</td><td>40</td></tr>
            <tr><td>61</td><td>344000</td><td>14000</td><td>40</td></tr>
            <tr><td>62</td><td>358000</td><td>14000</td><td>40</td></tr>
            <tr><td>63</td><td>372000</td><td>14000</td><td>40</td></tr>
            <tr><td>64</td><td>386000</td><td>14000</td><td>40</td></tr>
            <tr><td>65</td><td>400000</td><td>14000</td><td>40</td></tr>
            <tr><td>66</td><td>414000</td><td>14000</td><td>40</td></tr>
            <tr><td>67</td><td>428000</td><td>14000</td><td>40</td></tr>
            <tr><td>68</td><td>442000</td><td>14000</td><td>40</td></tr>
            <tr><td>69</td><td>456000</td><td>14000</td><td>40</td></tr>
            <tr><td>70</td><td>470000</td><td>16000</td><td>50</td></tr>
            <tr><td>71</td><td>486000</td><td>16000</td><td>50</td></tr>
            <tr><td>72</td><td>502000</td><td>16000</td><td>50</td></tr>
            <tr><td>73</td><td>518000</td><td>16000</td><td>50</td></tr>
            <tr><td>74</td><td>534000</td><td>16000</td><td>50</td></tr>
            <tr><td>75</td><td>550000</td><td>16000</td><td>50</td></tr>
            <tr><td>76</td><td>566000</td><td>16000</td><td>50</td></tr>
            <tr><td>77</td><td>582000</td><td>16000</td><td>50</td></tr>
            <tr><td>78</td><td>598000</td><td>16000</td><td>50</td></tr>
            <tr><td>79</td><td>614000</td><td>16000</td><td>50</td></tr>
            <tr><td>80</td><td>630000</td><td>18000</td><td>100</td></tr>
            <tr><td>81</td><td>648000</td><td>18000</td><td>100</td></tr>
            <tr><td>82</td><td>666000</td><td>18000</td><td>100</td></tr>
            <tr><td>83</td><td>684000</td><td>18000</td><td>100</td></tr>
            <tr><td>84</td><td>702000</td><td>18000</td><td>100</td></tr>
            <tr><td>85</td><td>720000</td><td>18000</td><td>100</td></tr>
            <tr><td>86</td><td>738000</td><td>18000</td><td>100</td></tr>
            <tr><td>87</td><td>756000</td><td>18000</td><td>100</td></tr>
            <tr><td>88</td><td>774000</td><td>18000</td><td>100</td></tr>
            <tr><td>89</td><td>792000</td><td>18000</td><td>100</td></tr>
            <tr><td>90</td><td>810000</td><td>20000</td><td>200</td></tr>
            <tr><td>91</td><td>830000</td><td>20000</td><td>200</td></tr>
            <tr><td>92</td><td>850000</td><td>20000</td><td>200</td></tr>
            <tr><td>93</td><td>870000</td><td>20000</td><td>200</td></tr>
            <tr><td>94</td><td>890000</td><td>20000</td><td>200</td></tr>
            <tr><td>95</td><td>910000</td><td>20000</td><td>200</td></tr>
            <tr><td>96</td><td>930000</td><td>20000</td><td>200</td></tr>
            <tr><td>97</td><td>950000</td><td>20000</td><td>200</td></tr>
            <tr><td>98</td><td>970000</td><td>29999</td><td>200</td></tr>
            <tr><td>99</td><td>999999</td><td>0</td><td>200</td></tr>
          </table>
        </div>
        <a id="Alucard-Spells"></a><h3>Alucard Spells</h3>
        <p>This is the list of the spells Alucard can execute. (A red arrow means you have to hold the button for a second.)</p>
        <table border="1">
          <tr align="center"><td>SPELL</td><td>DESCRIPTION</td><td><abbr title="Magic Points">MP</abbr></td><td>COMMAND</td></tr>
          <tr title="Summons a spirit which chases enemies."><td>Summon Spirit</td><td>Summons a fierce spirit</td><td align="center">5</td><td align="center"><img src="~static/img/summonspirit.gif" width="122" alt=""/></td></tr>
          <tr title="Alucard is involved by a red aura allowing him to temporarily absorb enemy's blood."><td>Dark Metamorphosis</td><td>Heal <abbr title="Health Points">HP</abbr> by shedding blood</td><td align="center">10</td><td align="center"><img src="~static/img/darkmetamorphosis.gif" width="130" alt=""/></td></tr>
          <tr title="Like his father, Alucard teleports and cast three fireballs or two bigger ones if you hold [up]. It's possible to control the teleportation and to cancel the attack if you hold [down]."><td>Hellfire</td><td>Teleport and fireball attack</td><td align="center">15</td><td align="center"><img src="~static/img/hellfire.gif" width="120" alt=""/></td></tr>
          <tr title="Similar to 'Summon Spirit' but summoning four spirits."><td>Tetra Spirit</td><td>Summons four spirits</td><td align="center">20</td><td align="center"><img src="~static/img/tetraspirit.gif" width="132" alt=""/></td></tr>
          <tr title="Damages all enemies and restores 8 HP for each hit."><td>Soul Steal</td><td>Steals <abbr title="Health Points">HP</abbr> from nearby enemies</td><td align="center">50</td><td align="center"><img src="~static/img/soulsteal.gif" width="160" alt=""/></td></tr>
          <tr title="Hold [X], make the command and release. Fly quickly as Bat hitting all enemies in his path."><td>Wing Smash</td><td>Powerful attack by Wolf</td><td align="center">8</td><td align="center"><img src="~static/img/wingsmash.gif" width="92" alt=""/></td></tr>
          <tr title="Runs quickly as wolf hitting all enemies in his path."><td>Wolf Charge</td><td>Powerful attack by Bat</td><td align="center">10</td><td align="center"><img src="~static/img/wolfcharge.gif" width="64" alt=""/></td></tr>
          <tr title="Made by the 'Sword Familiar'. Damages all enemies."><td>Sword Brothers</td><td>Summons Sword Brothers</td><td align="center">30</td><td align="center"><img src="~static/img/swordbrothers.gif" width="146" alt=""/></td></tr>
        </table>
        <a id="Richter-Skills"></a><h3>Richter Skills</h3>
        <p>This is the list of Richter Belmont Skills.</p>
        <table border="1">
          <tr align="center"><td width="174">SKILL</td><td width="357">DESCRIPTION</td><td>COMMAND</td></tr>
          <tr title="Use the 'Vampire Killer' to attack in directions normal attack cannot and can be used to shield Richter from projectiles."><td>Brandish Whip</td><td>Controls the whip freely</td><td align="center"><img src="~static/img/brandishwhip.gif" alt=""/></td></tr>
          <tr title="Jump and while Richter is raising, press jump again."><td>Backflip</td><td>Executes a somersault</td><td align="center"><img src="~static/img/backflip.gif" width="42" alt=""/></td></tr>
          <tr title="Can be made in mid air."><td>Hyper Jump</td><td>Make a high uppercut with a short sword</td><td align="center"><img src="~static/img/hyperjump.gif" width="54" alt=""/></td></tr>
          <tr title="It's possible to do another jump after this skill. Can be made in mid air."><td>Blade Dash</td><td>Air dash and short sword slash</td><td align="center"><img src="~static/img/bladedash.gif" width="80" alt=""/></td></tr>
          <tr title="Press jump again, and the slide will turn into a flying kick."><td>Slide</td><td>Slide and kicks ground enemies</td><td align="center"><img src="~static/img/slide.gif" width="40" alt=""/></td></tr>
        </table>
        <p>Enemies only have the attributes <abbr title="Level">LV</abbr>, <abbr title="Health Points">HP</abbr>, <abbr title="Strength">STR</abbr> and <abbr title="Defense">DEF</abbr>. These are fixed numbers assuming they don't gain level. Some enemies can have multiple parts with different attributes, can also have weapons and special moves which add damage to his <abbr title="Strength">STR</abbr> when it touches your character<br/>
        The attack, from enemies and controllable characters, can have the following effects indicated by the respective colors: <abbr title="Hit"><font color="#00ffff">H</font><font color="#ff00ff">I</font><font color="#ffff00">T</font></abbr>, <abbr title="Cut"><font color="#ff0000">CUT</font></abbr>, <abbr title="Fire"><font color="#ff5500">FIR</font></abbr>, <abbr title="Ice"><font color="#0088ff">ICE</font></abbr>, <abbr title="Thunder"><font color="#ccff00">THU</font></abbr>, <abbr title="Holy"><font color="#00ff00">HOL</font></abbr>, <abbr title="Dark"><font color="#008800">DRK</font></abbr>, <abbr title="Stone"><font color="#888888">STN</font></abbr>, <abbr title="Poison"><font color="#880088">PSN</font></abbr> and <abbr title="Curse"><font color="#555500">CUR</font></abbr>. The last three causes status ailments. (there's also a <abbr title="Water">H2O</abbr> element but there are no attacks based on it...a).</p>
        <a id="ailment"></a><h3>Status Ailments</h3>
        <p>Alucard can suffer from the following effects when hit by some special attacks from enemies.</p>
        <table>
          <tr><td valign="top"><font color="#888888"><b>Stone:</b></font></td><td>Alucard turns into stone (sometimes takes a gargoyle form). Quickly Tap the D-pad to break free. A <Item item="Hammer"/> can be used to do it instantly, but Alucard can't use it on himself; it can only be used by the Faerie Familiar.</td></tr>
          <tr><td height="18"></td></tr>
          <tr><td valign="top"><font color="#880088"><b>Poison:</b></font></td><td>Alucard is poisoned and his attack and defense power is halved for a period inversely proportional to his <abbr title="Constitution">CON</abbr>. Use a <Item item="Antivenom"/> to instantly neutralize the poison.</td></tr>
          <tr><td height="18"></td></tr>
          <tr><td valign="top"><font color="#555500"><b>Curse:</b></font></td><td>Alucard is taken by a curse which prevents him to attack (but he can still use spells and 'Sub-Weapons') for a period inversely proportional to his <abbr title="Constitution">CON</abbr>. Use a <Item item="Uncurse"/> to instantly break the curse.</td></tr>
        </table>
        <a id="Resistances"></a><h3>Resistances</h3>
        <p>The enemies may be strong or immune to some kind of attacks and may absorb others while some equipment makes Alucard resistant, immune or allow him to absorb damage done by attcks based on some elements.</p>
        <table>
          <tr><td valign="top"><b>Weak:</b></td><td>The damage done by an attack based on the element which the character is weak against is doubled.</td></tr>
          <tr><td height="18"></td></tr>
          <tr><td valign="top"><b>Strong:</b></td><td>The damage done by an attack based on the element which the character is strong against is halved.</td></tr>
          <tr><td height="18"></td></tr>
          <tr><td valign="top"><b>Immune:</b></td><td>The Attack based on the element which the character is immune is guarded.</td></tr>
          <tr><td height="18"></td></tr>
          <tr><td valign="top"><b>Absorb:</b></td><td>The damage done by an attack based on the element which the character absorbs is converted to <abbr title="Health Points">HP</abbr> ignoring <abbr title="Defense">DEF</abbr>.</td></tr>
        </table>
        <a id="Shield-Combos"></a><h3>Shield Combos</h3>
        <p>When Alucard equips <Item item="Shield rod"/> or <Item item="Mablung Sword"/> together with a shield and <img src="~static/img/quadrado.gif" alt="Square"/> + <img src="~static/img/circulo.gif" alt="Circle"/> is pressed, a summoning of the shield's powersd is realized.<br/>
        This is the list of the effects of the summoning effects from each shield.</p>
        <table border="1">
          <tr align="center"><td colspan="2">SHIELD COMBO</td><td>DESCRIPTION</td><td><abbr title="Magic Points">MP</abbr></td></tr>
          <tr title="Alucart shield combo - ?"><td width="14"><img src="~assets/items/alucard-shield.gif" width="28" alt=""/></td><td>Alucart shield</td><td align="center">?</td><td align="center">10</td></tr>
          <tr title="Leather shield combo - Raises DEF by 20 for nearly 60 seconds."><td><img src="~assets/items/leather-shield.gif" width="28" alt=""/></td><td>Leather shield</td><td>Temporarily raises <abbr title="Defense">DEF</abbr> by 20</td><td align="center">10</td></tr>
          <tr title="Medusa shield combo - Medusa Head casts rays from the eyes which damages enemies. ATT 0 (HIT)."><td><img src="~assets/items/medusa-shield.gif" width="28" alt=""/></td><td>Medusa shield</td><td>Cast rays which damages enemies on the screen</td><td align="center">30</td></tr>
          <tr title="Knight shield combo - Raises ATT by 20 for nearly 60 seconds."><td><img src="~assets/items/knight-shield.gif" width="28" alt=""/></td><td>Knight shield</td><td>Temporarily raises <abbr title="Attack">ATT</abbr> by 20</td><td align="center">10</td></tr>
          <tr title="Iron shield combo - Summons a giant knight who throws huge swords causing massive damage to enemies. ATT 40 (HIT)"><td><img src="~assets/items/iron-shield.gif" width="28" alt=""/></td><td>Iron shield</td><td>Summons a knight who throws huge swords</td><td align="center">20</td></tr>
          <tr title="AxeLord shield combo - Summons an Axe Knight who attacks the first enemy he finds in its way. ATT 20 (HIT)."><td><img src="~assets/items/axelord-shield.gif" width="28" alt=""/></td><td>AxeLord shield</td><td>Summons an Axe Knight</td><td align="center">20</td></tr>
          <tr title="Dark shield combo - Summons a evil head who attacks with meteors damaging all enemies. ATT 30 (HIT)."><td><img src="~assets/items/dark-shield.gif" width="28" alt=""/></td><td>Dark shield</td><td>Summons meteors which damages all enemies</td><td align="center">30</td></tr>
          <tr title="Goddess shield combo - Gives protection against dark attacks for nearly 60 seconds."><td><img src="~assets/items/goddess-shield.gif" width="28" alt=""/></td><td>Goddess shield</td><td>Brief protection against Dark</td><td align="center">40</td></tr>
          <tr title="Shaman shield combo - Raises INT by 20 for nearly 60 seconds."><td><img src="~assets/items/shaman-shield.gif" width="28" alt=""/></td><td>Shaman shield</td><td>Temporarily raises <abbr title="Defense">INT</abbr> by 20</td><td align="center">10</td></tr>
          <tr title="Skull shield combo - Summons a pile of skulls which fires a powerful beam. ATT 100 (HIT)"><td><img src="~assets/items/skull-shield.gif" width="28" alt=""/></td><td>Skull shield</td><td>Summons skulls which fires a powerful beam</td><td align="center">40</td></tr>
          <tr title="Fire shield combo - Summons fire salamanders inspired in the Gradius game which wander on the screen damaging enemies. ATT 70 (FIR)."><td><img src="~assets/items/fire-shield.gif" width="28" alt=""/></td><td>Fire shield</td><td>Summons fire salamanders</td><td align="center">50</td></tr>
          <tr title="Herald shield combo - Grants protection against Fire and Thunder for nearly 60 seconds."><td><img src="~assets/items/herald-shield.gif" width="28" alt=""/></td><td>Herald shield</td><td>Brief protection against fire and thunder</td><td align="center">10</td></tr>
          <tr title="Alucard shield combo - Confers to Alucard shield the ability to recover 8 HP, 1 'Heart', create a invulnerability time of 3 seconds and cause 255 damage (HIT) when it touch any target."><td><img src="~assets/items/alucard-shield.gif" width="28" alt=""/></td><td>Alucard shield</td><td>Summons the power of all shields</td><td align="center">20</td></tr>
        </table>
      </main>
      <hr/>
      <Footer/>
    </div>
  </div>
</template>

<script>
  export default {}
</script>

<style scoped>
  table {
    width: 90%;
    margin: 0 auto;
  }
</style>