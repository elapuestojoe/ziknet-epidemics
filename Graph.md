

```python
from networkParser import parseContacts

# contactList, biteList, timeList = parseContacts("GMAP0/CatemacoBaseline_HET 36756.xml")
contactList, biteList, timeList = parseContacts("GMAP0.50/CatemacoBaseline_HET 68944.xml")
contactList = sorted(contactList)
```

## Set SEIR colors


```python
colors = {
    "susceptible" : 0x00C853, #green
    "exposed" : 0xF57F17,     #orange
    "infected" : 0xD50000,        #infected
    "recovered" : 0x2962FF,     #recovered
}
```


```python
import random

graph = {
    "nodes": {},
    "edges": [],
}

for person in contactList:
    graph["nodes"][person] = {'color': colors["susceptible"], 'size': 2.0}
    
randomInfected = random.sample(contactList,3)
for infected in randomInfected:
    graph["nodes"][infected]['color'] = colors["infected"]
```


```python
import jgraph
jgraph.draw(graph)
```


<div id="graph-3e144fc9-45a1-40c6-ada0-eebd4b5da484"></div>
           <script type="text/javascript">
           require.config({baseUrl: '/',
                             paths: {jgraph: ['nbextensions/jgraph.min', 'https://rawgit.com/patrickfuller/jgraph/master/js/build/jgraph.min']}});
           require(['jgraph'], function () {
               var $d = $('#graph-3e144fc9-45a1-40c6-ada0-eebd4b5da484');
               $d.width(600); $d.height(400);
               $d.jgraph = jQuery.extend({}, jgraph);
               $d.jgraph.create($d, {nodeSize: 2.000000,
                                     edgeSize: 0.250000,
                                     defaultNodeColor: '0x5bc0de',
                                     defaultEdgeColor: '0xaaaaaa',
                                     shader: 'basic',
                                     z: 100,
                                     runOptimization: true,
                                     directed: true,
                                     showSave: false});
               $d.jgraph.draw({
    "edges": [],
    "nodes": {
        "aa": { "color": "0xc853", "size": 2.0 },
        "ab": { "color": "0xc853", "size": 2.0 },
        "ac": { "color": "0xc853", "size": 2.0 },
        "ad": { "color": "0xc853", "size": 2.0 },
        "ae": { "color": "0xc853", "size": 2.0 },
        "af": { "color": "0xc853", "size": 2.0 },
        "ag": { "color": "0xc853", "size": 2.0 },
        "ah": { "color": "0xc853", "size": 2.0 },
        "ai": { "color": "0xc853", "size": 2.0 },
        "aj": { "color": "0xc853", "size": 2.0 },
        "ak": { "color": "0xc853", "size": 2.0 },
        "al": { "color": "0xc853", "size": 2.0 },
        "am": { "color": "0xc853", "size": 2.0 },
        "an": { "color": "0xc853", "size": 2.0 },
        "ao": { "color": "0xc853", "size": 2.0 },
        "ap": { "color": "0xc853", "size": 2.0 },
        "aq": { "color": "0xc853", "size": 2.0 },
        "ar": { "color": "0xc853", "size": 2.0 },
        "as": { "color": "0xc853", "size": 2.0 },
        "at": { "color": "0xc853", "size": 2.0 },
        "au": { "color": "0xc853", "size": 2.0 },
        "av": { "color": "0xc853", "size": 2.0 },
        "aw": { "color": "0xd50000", "size": 2.0 },
        "ax": { "color": "0xc853", "size": 2.0 },
        "ay": { "color": "0xc853", "size": 2.0 },
        "ba": { "color": "0xc853", "size": 2.0 },
        "bb": { "color": "0xc853", "size": 2.0 },
        "bc": { "color": "0xc853", "size": 2.0 },
        "bd": { "color": "0xc853", "size": 2.0 },
        "be": { "color": "0xc853", "size": 2.0 },
        "bf": { "color": "0xc853", "size": 2.0 },
        "bg": { "color": "0xc853", "size": 2.0 },
        "bh": { "color": "0xc853", "size": 2.0 },
        "bi": { "color": "0xc853", "size": 2.0 },
        "bj": { "color": "0xc853", "size": 2.0 },
        "bk": { "color": "0xc853", "size": 2.0 },
        "bl": { "color": "0xc853", "size": 2.0 },
        "bm": { "color": "0xc853", "size": 2.0 },
        "bn": { "color": "0xc853", "size": 2.0 },
        "bo": { "color": "0xc853", "size": 2.0 },
        "bp": { "color": "0xc853", "size": 2.0 },
        "bq": { "color": "0xc853", "size": 2.0 },
        "br": { "color": "0xc853", "size": 2.0 },
        "bs": { "color": "0xc853", "size": 2.0 },
        "bt": { "color": "0xc853", "size": 2.0 },
        "bu": { "color": "0xc853", "size": 2.0 },
        "bv": { "color": "0xc853", "size": 2.0 },
        "bw": { "color": "0xc853", "size": 2.0 },
        "bx": { "color": "0xc853", "size": 2.0 },
        "by": { "color": "0xc853", "size": 2.0 },
        "bz": { "color": "0xc853", "size": 2.0 },
        "ca": { "color": "0xc853", "size": 2.0 },
        "cb": { "color": "0xc853", "size": 2.0 },
        "cc": { "color": "0xd50000", "size": 2.0 },
        "cd": { "color": "0xc853", "size": 2.0 },
        "ce": { "color": "0xc853", "size": 2.0 },
        "cf": { "color": "0xc853", "size": 2.0 },
        "cg": { "color": "0xc853", "size": 2.0 },
        "ch": { "color": "0xc853", "size": 2.0 },
        "ci": { "color": "0xc853", "size": 2.0 },
        "cj": { "color": "0xc853", "size": 2.0 },
        "ck": { "color": "0xd50000", "size": 2.0 }
    }
});

               $d.resizable({
                   aspectRatio: 600 / 400,
                   resize: function (evt, ui) {
                       $d.jgraph.renderer.setSize(ui.size.width,
                                                  ui.size.height);
                   }
               });
           });
           </script>



```python
# WARMUP = int(random.uniform(25000, 70000))
WARMUP = int(random.uniform(4000, 10000))
infectionsPerContact = {}

for i in contactList:
    infectionsPerContact[i] = []

timeListSortedKeys = list(filter(lambda x: x > WARMUP,  sorted(timeList.keys())))

exposed = {}

initialTime = 0 if len(timeListSortedKeys) == 0 else int(timeListSortedKeys[0])

# print(timeList)
# print(timeListSortedKeys)
```


```python
infectedPeople = {}
susceptible = contactList.copy()

for i in randomInfected:
        infectedPeople[i] = initialTime
        susceptible.remove(i)
recovered = {}
asymptomatic = {}
infectedMosquitoes = []
mosquitoesContact = {}
SEIR = {}
edges = []
```


```python
fourDays = 1152
threeDays = 864
tenDays = 2880
```


```python
for key in timeListSortedKeys:

		currentMosquitoes = timeList[key]
		currTime = int(key)
		for mosquito in currentMosquitoes:
			# Get time/bite
			currentBiteList = biteList[mosquito]
			i = currentBiteList["times"].index(key)
			bited = currentBiteList["bites"][i]
			
			if(bited in infectedPeople and mosquito not in infectedMosquitoes):
				# pVH Transmission probability from an infectious human to a susceptible mosquito per bite    0.3–0.75   
				 # (Gao et al., 2016; Andraud et al., 2012; Chikaki and Ishikawa, 2009)
				probability = random.uniform(0.3, 0.75)
				if(random.uniform(0.0,1.0) <= probability):
					infectedMosquitoes.append(mosquito)
					mosquitoesContact[mosquito] = bited
					# print("Mosquito {} got infected by {} at time {}".format(mosquito, bited, currTime))
			else:
				# pHV Transmission probability from an infectious mosquito to a susceptible human per bite    0.1–0.75    
				# (Gao et al., 2016; Andraud et al., 2012; Chikaki and Ishikawa, 2009)

				# 1/fH    Duration of human latent period, E (days)   4   (Turmel et al., 2016; Bearcroft, 1956)
				# 345600
				if(mosquito in infectedMosquitoes and bited in susceptible):
					if(random.uniform(0.0,1.0) <= random.uniform(0.1,0.75)):
						exposed[bited] = currTime
						susceptible.remove(bited)
						edges.append((mosquitoesContact[mosquito], currentBiteList["bites"][i]))
						infectionsPerContact[mosquitoesContact[mosquito]].append(bited)
						# print("Human {} got infected by {} {} at time {}".format(currentBiteList["bites"][i], mosquito, mosquitoesContact[mosquito], currTime))
						# status()
						# draw_graph(contactList, edges, infectedPeople, susceptible, exposed, recovered)
		removals = []
		for e in exposed:
			# https://www.sciencedirect.com/science/article/pii/S1755436517301093
			if(currTime >= exposed[e]+ (threeDays * 2) ):
			# if(currTime >= exposed[e]+ (threeDays * 1) ):
				infectedPeople[e] = currTime
				removals.append(e)
				# print("{} went from exposed to infected at {}".format(e,exposed[e]+fourDays))
				
		for r in removals:
			exposed.pop(r)
			# draw_graph(contactList, edges, infectedPeople, susceptible, exposed, recovered)


		removals = []
		for e in infectedPeople:
			if(currTime >= infectedPeople[e]+ (fourDays + threeDays)):
			# if(currTime >= infectedPeople[e]+ (fourDays)):
				recovered[e] = currTime
				removals.append(e)
				# print("{} went from infectious to recovered at time {}".format(e, infectedPeople[e]+fourDays))
		for r in removals:
			infectedPeople.pop(r)
			# draw_graph(contactList, edges, infectedPeople, susceptible, exposed, recovered)

		# UPDATE SEIR
		SEIR[currTime] = [len(susceptible), len(exposed), len(infectedPeople), len(recovered)]

	# Fin de simulación de epidemia
```


```python
print(infectionsPerContact)
```

    {'aa': [], 'ab': [], 'ac': [], 'ad': [], 'ae': [], 'af': [], 'ag': [], 'ah': [], 'ai': [], 'aj': [], 'ak': [], 'al': [], 'am': [], 'an': [], 'ao': [], 'ap': [], 'aq': [], 'ar': [], 'as': [], 'at': [], 'au': [], 'av': [], 'aw': [], 'ax': [], 'ay': [], 'ba': [], 'bb': [], 'bc': [], 'bd': [], 'be': [], 'bf': [], 'bg': [], 'bh': [], 'bi': [], 'bj': [], 'bk': [], 'bl': [], 'bm': [], 'bn': ['ah', 'cb'], 'bo': [], 'bp': [], 'bq': [], 'br': [], 'bs': [], 'bt': [], 'bu': [], 'bv': ['bw', 'cg'], 'bw': [], 'bx': [], 'by': [], 'bz': [], 'ca': [], 'cb': [], 'cc': ['cj'], 'cd': [], 'ce': [], 'cf': [], 'cg': [], 'ch': [], 'ci': [], 'cj': ['ag'], 'ck': ['bn', 'bc', 'bv', 'ai', 'by']}
    


```python
print("Exposed:", exposed)
print("Infected: ", infectedPeople)
print("Recovered: ", recovered)

```

    Exposed: {'cb': 18709}
    Infected:  {'cg': 19694}
    Recovered:  {'ck': 7670, 'aw': 7670, 'cc': 7670, 'bn': 12558, 'bc': 12905, 'bv': 13030, 'cj': 13503, 'ai': 14645, 'by': 17189, 'ag': 18059, 'bw': 18116, 'ah': 18655}
    

<font size="18"><br>
    Graph Showing:<br><br></font>
    <font size="18" color="green">Susceptible<br><br></font>
    <font size="18" color="orange">Exposed<br><br></font> 
    <font size="18" color="red">Infected<br><br></font>
    <font size="18" color="blue">Recovered<br><br></font>


```python
for infectedKey in infectedPeople.keys():
    graph["nodes"][infectedKey]["color"] = colors["infected"]
    
for recoveredKey in recovered.keys():
    graph["nodes"][recoveredKey]["color"] = colors["recovered"]

for exposedKey in exposed.keys():
    graph["nodes"][exposedKey]["color"] = colors["exposed"]
    
for infectionKey in infectionsPerContact.keys():
    infection = infectionsPerContact[infectionKey]
    for outNode in infection:
        graph["edges"].append({"source": infectionKey, "target": outNode, "color": 0x000000})
jgraph.draw(graph)
```


<div id="graph-cb5e7954-9c20-4141-9a18-6c8d1b4a19a8"></div>
           <script type="text/javascript">
           require.config({baseUrl: '/',
                             paths: {jgraph: ['nbextensions/jgraph.min', 'https://rawgit.com/patrickfuller/jgraph/master/js/build/jgraph.min']}});
           require(['jgraph'], function () {
               var $d = $('#graph-cb5e7954-9c20-4141-9a18-6c8d1b4a19a8');
               $d.width(600); $d.height(400);
               $d.jgraph = jQuery.extend({}, jgraph);
               $d.jgraph.create($d, {nodeSize: 2.000000,
                                     edgeSize: 0.250000,
                                     defaultNodeColor: '0x5bc0de',
                                     defaultEdgeColor: '0xaaaaaa',
                                     shader: 'basic',
                                     z: 100,
                                     runOptimization: true,
                                     directed: true,
                                     showSave: false});
               $d.jgraph.draw({
    "edges": [
        { "color": "0x0", "source": "bn", "target": "ah" },
        { "color": "0x0", "source": "bn", "target": "cb" },
        { "color": "0x0", "source": "bv", "target": "bw" },
        { "color": "0x0", "source": "bv", "target": "cg" },
        { "color": "0x0", "source": "cc", "target": "cj" },
        { "color": "0x0", "source": "cj", "target": "ag" },
        { "color": "0x0", "source": "ck", "target": "bn" },
        { "color": "0x0", "source": "ck", "target": "bc" },
        { "color": "0x0", "source": "ck", "target": "bv" },
        { "color": "0x0", "source": "ck", "target": "ai" },
        { "color": "0x0", "source": "ck", "target": "by" },
        { "color": "0x0", "source": "bn", "target": "ah" },
        { "color": "0x0", "source": "bn", "target": "cb" },
        { "color": "0x0", "source": "bv", "target": "bw" },
        { "color": "0x0", "source": "bv", "target": "cg" },
        { "color": "0x0", "source": "cc", "target": "cj" },
        { "color": "0x0", "source": "cj", "target": "ag" },
        { "color": "0x0", "source": "ck", "target": "bn" },
        { "color": "0x0", "source": "ck", "target": "bc" },
        { "color": "0x0", "source": "ck", "target": "bv" },
        { "color": "0x0", "source": "ck", "target": "ai" },
        { "color": "0x0", "source": "ck", "target": "by" },
        { "color": "0x0", "source": "bn", "target": "ah" },
        { "color": "0x0", "source": "bn", "target": "cb" },
        { "color": "0x0", "source": "bv", "target": "bw" },
        { "color": "0x0", "source": "bv", "target": "cg" },
        { "color": "0x0", "source": "cc", "target": "cj" },
        { "color": "0x0", "source": "cj", "target": "ag" },
        { "color": "0x0", "source": "ck", "target": "bn" },
        { "color": "0x0", "source": "ck", "target": "bc" },
        { "color": "0x0", "source": "ck", "target": "bv" },
        { "color": "0x0", "source": "ck", "target": "ai" },
        { "color": "0x0", "source": "ck", "target": "by" }
    ],
    "nodes": {
        "aa": { "color": "0xc853", "size": 2.0 },
        "ab": { "color": "0xc853", "size": 2.0 },
        "ac": { "color": "0xc853", "size": 2.0 },
        "ad": { "color": "0xc853", "size": 2.0 },
        "ae": { "color": "0xc853", "size": 2.0 },
        "af": { "color": "0xc853", "size": 2.0 },
        "ag": { "color": "0x2962ff", "size": 2.0 },
        "ah": { "color": "0x2962ff", "size": 2.0 },
        "ai": { "color": "0x2962ff", "size": 2.0 },
        "aj": { "color": "0xc853", "size": 2.0 },
        "ak": { "color": "0xc853", "size": 2.0 },
        "al": { "color": "0xc853", "size": 2.0 },
        "am": { "color": "0xc853", "size": 2.0 },
        "an": { "color": "0xc853", "size": 2.0 },
        "ao": { "color": "0xc853", "size": 2.0 },
        "ap": { "color": "0xc853", "size": 2.0 },
        "aq": { "color": "0xc853", "size": 2.0 },
        "ar": { "color": "0xc853", "size": 2.0 },
        "as": { "color": "0xc853", "size": 2.0 },
        "at": { "color": "0xc853", "size": 2.0 },
        "au": { "color": "0xc853", "size": 2.0 },
        "av": { "color": "0xc853", "size": 2.0 },
        "aw": { "color": "0x2962ff", "size": 2.0 },
        "ax": { "color": "0xc853", "size": 2.0 },
        "ay": { "color": "0xc853", "size": 2.0 },
        "ba": { "color": "0xc853", "size": 2.0 },
        "bb": { "color": "0xc853", "size": 2.0 },
        "bc": { "color": "0x2962ff", "size": 2.0 },
        "bd": { "color": "0xc853", "size": 2.0 },
        "be": { "color": "0xc853", "size": 2.0 },
        "bf": { "color": "0xc853", "size": 2.0 },
        "bg": { "color": "0xc853", "size": 2.0 },
        "bh": { "color": "0xc853", "size": 2.0 },
        "bi": { "color": "0xc853", "size": 2.0 },
        "bj": { "color": "0xc853", "size": 2.0 },
        "bk": { "color": "0xc853", "size": 2.0 },
        "bl": { "color": "0xc853", "size": 2.0 },
        "bm": { "color": "0xc853", "size": 2.0 },
        "bn": { "color": "0x2962ff", "size": 2.0 },
        "bo": { "color": "0xc853", "size": 2.0 },
        "bp": { "color": "0xc853", "size": 2.0 },
        "bq": { "color": "0xc853", "size": 2.0 },
        "br": { "color": "0xc853", "size": 2.0 },
        "bs": { "color": "0xc853", "size": 2.0 },
        "bt": { "color": "0xc853", "size": 2.0 },
        "bu": { "color": "0xc853", "size": 2.0 },
        "bv": { "color": "0x2962ff", "size": 2.0 },
        "bw": { "color": "0x2962ff", "size": 2.0 },
        "bx": { "color": "0xc853", "size": 2.0 },
        "by": { "color": "0x2962ff", "size": 2.0 },
        "bz": { "color": "0xc853", "size": 2.0 },
        "ca": { "color": "0xc853", "size": 2.0 },
        "cb": { "color": "0xf57f17", "size": 2.0 },
        "cc": { "color": "0x2962ff", "size": 2.0 },
        "cd": { "color": "0xc853", "size": 2.0 },
        "ce": { "color": "0xc853", "size": 2.0 },
        "cf": { "color": "0xc853", "size": 2.0 },
        "cg": { "color": "0xd50000", "size": 2.0 },
        "ch": { "color": "0xc853", "size": 2.0 },
        "ci": { "color": "0xc853", "size": 2.0 },
        "cj": { "color": "0x2962ff", "size": 2.0 },
        "ck": { "color": "0x2962ff", "size": 2.0 }
    }
});

               $d.resizable({
                   aspectRatio: 600 / 400,
                   resize: function (evt, ui) {
                       $d.jgraph.renderer.setSize(ui.size.width,
                                                  ui.size.height);
                   }
               });
           });
           </script>

