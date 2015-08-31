# Bear Solver
A quick & dirty command-line tool for generating solutions for Alphabear puzzles.

## Parameters
|Param | Description |
------ | ----------- |
| --words=FILENAME | a file containing the list of words. On Macs and \*nixen, a good candidate is /usr/share/dict/words |
| --letters=ABCD | all the letters you can see on the board. All of them, even repetitions. |
| --must_have=ABCD | (optional) a list of the letters you must have in your solutions. This is usually going to be the ones with a current score of 1, but you might want to include one or two from the 2's that look like they're going to cause you trouble in the next turn. |
| --nice_to_have=ABCD | (optional) another list of letters that you'd like to see in the solutions if possible. This is usually going to be the ones with a current score of 2. |

## Examples
Let's say your board looks like this iTunes screenshot:

<img src='http://a2.mzstatic.com/us/r30/Purple5/v4/0d/8f/33/0d8f3362-ec3f-bd50-31bb-0be7c4718a23/screen322x572.jpeg' width='50%'>
```
$ python bearsolver.py --words=/usr/share/dict/words --letters=hetetlelachahcates
['castellate', 'catalecta', 'catastate', 'Chaetetes', 'Chechehet', 'echelette', 
'Hallstatt', 'saltcatch', 'teethache', 'aesthete', 'asellate', 'Athecata', 'athe
cate', 'Cactales', 'Calathea', 'castelet', 'catalase', ...
```

Or this one:

<img src='http://a4.mzstatic.com/us/r30/Purple7/v4/ae/4c/8b/ae4c8bbc-910d-cca6-ab70-e4bfb9cb2947/screen322x572.jpeg' width='50%'>
```
$ python bearsolver.py --words=/usr/share/dict/words --letters=fwnokeiwahfiss --
must_have=kno --nice_to_have=fwe
['knowe', 'kenosis', 'Kossean', 'Nesokia', 'Kiowan', 'soaken', 'Wikeno', 'Kohen'
, 'Koine', 'koine', 'oaken', 'snoek', 'snoke', 'snowk', 'soken', 'wakon', 'keno'
, 'know', 'Wishoskan', 'hinoki', 'inkosi', 'kishon', 'Hokan', 'ikona', 'Konia', 
'kosin', 'honk', 'kino', 'kona', 'nako', 'sonk', 'kon']
```

I'm sure you get the idea.

