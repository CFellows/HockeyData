HockeyData
==========

NHL Player Roster Data
2014 Current NHL Players Snapshot 8.25.2014

Names Removed. Please contact if this data infringes on any copyrights or trademarks.

Big Data is Everywhere. Make it work for you.

Obtaining and formatting data is actually pretty easy if you have the right tools.
Scrubbing data can be pretty straightforward as well
Experimentation is made easier through data science tools like Tableau.
Models can be shared and re-examined, and
Investigations are ongoing.

When Anaheim beat Ottawa to win the Stanley Cup in 2007, my colleague quipped that Anaheim had more players from Canada than Ottawa and that this was a win for Canada.  But is this still the case? What's going on in the NHL and who is "Canada's team"?  This past weekend I created and analysed an interesting data set this weekend using some command line tools and it turned out to be much easier than I expected.

It's strange that there is no one place to get all the player data for the league. Lucky for us, getting the rosters from all the teams can actually be done in one command:

curl http://{ducks, coyotes,flames,blackhawks,avalanche,stars,oilers,kings,wild,predators,sharks,blues,canucks,jets,bruins,sabres,hurricanes,bluejackets,redwings,panthers,canadiens,devils,islanders,rangers,senators,flyers,penguins,lightning,mapleleafs,capitals}.nhl.com/club/roster.htm > rosters.txt

Of course, there is also the WGET command among others, and every modern language has libraries to get and work with HTML.  I expect that the next data science project will be entirely in Python (which has libraries to work with xml.)  Although the trial and error process presented by the command line feels more natural and experimental.  I can quickly run commands and sample or view the output and change the commands if

Foregoing the power and simplicity of python xml parsing, I formatted the data into tables using the stream editor command sed and regular expressions.  I then needed to use Notepad++ to scrub the data, but it turns out it uses regular expressions in the same was as sed, and I could experiment and visualize very quickly.

In the same way, we can use the Tableau tools to visualize and experiment with our data, running investigations through trial and error with beatiful visualizations that can be shared and explored.

Anyway, the Senators' roster includes three players from Ottawa, and the three teams with the most Canadian players are Toronto's, Calgary's, and Colorado's.  There can only be five players plus a goalie from each team on the ice, and (I had to look this up) there can be no more than 18 players plus 2 goalies on the roster.

Some other findings, 25 current NHL players were born in Toronto, making it the unofficial "birthplace" of this year's NHL. Toronto has so many players it could fill it with native born players and still have five players not make the roster.

We can see the relative age effect described in Malcom Gladwell's Outliers. When looking at a histogram of the counts of birth months, we may see a little bit of this effect, in which children who are the oldest when hockey season starts tend to do the best at youth hockey and continue on to pursue professional careers in the NHL.

And we see most of the birth years fall between 1982 and 1992, but mostly around 1990, which makes me feel old.
