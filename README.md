**CVE Graph Visualization**

**Overview**:   
A project to visualize relations between CVEs and CWEs from the NIST Database.

**Sample Output:**   
![Image](https://i.imgur.com/iSAN7gx.png)


**File Specifications**:  
*cve_visualization.ipynb*: Jupyter notebook that includes python code to view visualizations.  Nodes are grouped based on CWE, and CVEs with no associated 
CWE are grouped under the node with value 0. The base score of each CVE is visually shown based on each CVE node's size. To convert the scores into node sizes that
would be discernable using networkx, scores were multiplied by 10. CWEs, as well as CVEs with no risk score, are displayed with the standard size 20. The severity
score of a CVE is displayed based on node color. Specidications below: 


BASE SCORE | NODE SIZE | 
--- | --- |
None | 20 |
--- | --- |
Low | 20 - 39 |
--- | --- |
Medium | 40 - 69 |
--- | --- |
High | 70 - 100 |
--- | --- |

SEVERITY SCORE | NODE COLOR | 
--- | --- |
Critical | Red |
--- | --- |
High | Pink |
--- | --- |
Medium | Orange |
--- | --- |
Low | Yellow |
--- | --- |
None  | Blue | 
--- | --- |

Potential Improvements:
 * Add separate function for converting json file to pandas dataframe (currently only handles json dict, but has comments that detail how to handle json file) 
 * Handling Large Datasets: Clean visualization with networkx is difficult when using large datasets
 * Node Size and Color Customization: There might be a more direct way to achieve this 
 * Node Shape: Make CVE nodes squares and CWE nodes circles

