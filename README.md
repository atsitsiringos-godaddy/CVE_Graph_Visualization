**CVE Graph Visualization**

**Overview**:   
A project to visualize relations between CVEs and CWEs from the NIST Database.

**Sample Output:**   
![Image](https://i.imgur.com/iSAN7gx.png)


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
criticality of a CVE is displayed based on node color. Specidications below

Nod
RED = CRITICAL
PINK = HIGH
ORANGE = MEDIUM
YELLOW = LOW
BLUE = NONE 

NODE COLOR | SEVERITY SCORE | 
--- | --- |
RED |  CRITICAL| 
--- | --- |
PINK | HIGH | 
--- | --- |
ORANGE | MEDIUM |
--- | --- |
YELLOW | LOW |
--- | --- |
BLUE | NONE |
--- | --- |

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

