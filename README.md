**CVE Graph Visualization**

**Overview**:   
A project to visualize relations between CVEs and CWEs from the NIST Database.

**Sample Output:**   
![alt text](<blockquote class="imgur-embed-pub" lang="en" data-id="a/DwGg4TP"  ><a href="//imgur.com/a/DwGg4TP">CVE Graph Visualization </a></blockquote><script async src="//s.imgur.com/min/embed.js" charset="utf-8"></script>)


**Required Python Libraries**:   
pandas   
networkx   
matplotlib.pyplot. 
numpy   
math

**File Specifications**:  
*cve_visualization.ipynb*: Jupyter notebook that includes python code to view visualizations.  Nodes are grouped based on CWE, and CVEs with no associated 
CWE are grouped under the node with value 0. The risk score of each CVE is visually shown based on each CVE node's size. To convert the scores into node sizes that
would be discernable using networkx, scores were multiplied by 10. CWEs, as well as CVEs with no risk score, are displayed with the standard size 20. The risk
criticality of a CVE is displayed based on node color, where: 

Nod
RED = CRITICAL
PINK = HIGH
ORANGE = MEDIUM
YELLOW = LOW
BLUE = NONE 

Attempt | #1 | #2 | #3 | #4 | #5 | #6 | #7 | #8 | #9 | #10 | #11
--- | --- | --- | --- |--- |--- |--- |--- |--- |--- |--- |---
Seconds | 301 | 283 | 290 | 286 | 289 | 285 | 287 | 287 | 272 | 276 | 269

Relationships shown between CVEs and CWEs, along with 
CVE publication date (first published), cvss V3 vector string, baseScore, and baseSeverity.

The risk score of each CVE is visually shown based on each CVE node's size. To convert the scores into node sizes that would be discernable using 
networkx, scores were multiplied by 10. CWEs, as well as CVEs with no risk score, are displayed with the standard size 20. 

*graph.png*: sample output of the program (saved as matplotlib figure and then converted to .png file) 

Potential Improvements:
 * JSON to CSV or Pandas Dataframe Conversion 
 * Handling Large Datasets: Clean visualization with networkx is difficult when using large datasets
 * Labeling: The text box specifying label details might need to be replaced by clearer labels under each node
 * Node Size Customization: There might be a more direct way to achieve this 

