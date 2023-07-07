# jediepgxtream

<img src="https://i.ibb.co/QpgRSsk/1.png" alt="1" border="0">

Assign 3rd Party EPG to IPTV Channels

Plugin will work on 720 or HD boxes.
There is nothing over complicated in this plugin and should therefore work on all images.
It has only been tested on OpenATV for this release.

How to use

Plugin is found in plugins menu.

Plugin loads all bouquets from bouquets folders except bouquets created via Auto Bouquets Maker.
Therefore can be used with any bouquet creating plugin not just my Jedi Maker Xtream.

Column 1 - Bouquets
This will load all your bouquets as found in /etc/enigma2/

If bouquets are grouped it will load parent group. Pressing right or OK will load sub-bouquets.

Column2 - Channels
This loads all the channels from the selected bouquet.
If a channel has an EPG already assigned via this Jedi EPG Xtream plugin a LINK icon will show next to it.
Can unassign an EPG from the channel by pressing GREEN Button while that channel is highlighted.

Column3 - EPG sources
This loads a list of EPG sources that are defined in an editable file - epglist.txt
/etc/enigma2/jediepgxtream/epglist.txt

I have added in all the Rytec sources into this file, and 2 other working sources.
If using Jedi Maker Xtream playlists, these xmltv.php sources will also automatically be added to the EPG source list on load.

You can also use any active xmltv.php file to populate other providers.

Other 3rd party EPGs can be added. But EPG importer cannot use https:// sources though :(

Sources can be xml, xz, gz or an active iptv xmltv.php links

To edit the epglist.txt file, 2 elements are required. A name and a source separated by a single space.
The name has to be file name friendly. So use only Alpha-numeric characters and hyphens. Do not use \/.?* or spaces.

good example:
Rytec-News-Channels http://www.xmltvepg.nl/rytecNWS.xz

bad examples:
Rytec News-Channels http://www.xmltvepg.nl/rytecNWS.xz
Rytec/News/Channels http://www.xmltvepg.nl/rytecNWS.xz

I have pre-downloaded all the sources data in compact form.
Sources can be refreshed by pressing YELLOW button or OK button if source list is empty (optional), or can be hidden by pressing BLUE button.
Hiding the source just comments it out of epglist.txt file. It does not permantly delete it.

Column 4 
This column only lists active channels that has EPG data. It does not list channels that are named but has blank EPG data.
Therefore this plugin can actually be used to check your providers XMLTV file to see what actual channels should have EPG.

Press OK or GREEN button will assign this EPG to the channel.
On assigning it will jump back to column 2 to allow further adding of channel EPGs.

On assigning - everything is automatically created in the background. No further saving need, just exit out of the plugin to finish then select your newly created source in epgimporter. (then manually download epgimport source).

Navigation Buttons

Left
Right
Up
Down

Channel up - Page up
Channel Down - Page down

0 - Back to top
2 - Previous Letter
8 - Next Letter

EPG Importer

Open EPG importer.
Press BLUE button for "Sources".
Expand "Jedi EPG"
Select all sources.
Save
Press YELLOW button to manually download sources.
How to delete all assigned EPGs and start from scratch.

delete epg.json from /etc/enigma2/jediepgxtream/
