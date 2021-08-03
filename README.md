**CVE Graph Visualization**

**Overview**:   
A project to visualize relations between CVEs and CWEs from the NIST Database.

**Required Python Libraries**:   
pandas   
networkx   
matplotlib.pyplot. 
numpy   
math

**File Specifications**:  
*recent.json*: Recent taken from the RECENT-CVE [NIST datafeed](https://nvd.nist.gov/vuln/data-feeds). 

*recent.csv*: Used an [online converter](https://www.convertcsv.com/json-to-csv.htm) to convert the .json file to CSV file (While this is possible to do through the python pandas library, I found that data was formatted improperly). 

*cve_visualization.ipynb*: Jupyter notebook that includes python code to view visualizations. Relationships shown between CVEs and CWEs, along with 
CVE publication date (first published), cvss V3 vector string, baseScore, and baseSeverity. Nodes are grouped based on CWE, and CVEs with no associated 
CWE are grouped under the node with value 0. 

The risk score of each CVE is visually shown based on each CVE node's size. To convert the scores into node sizes that would be discernable using 
networkx, scores were multiplied by 10. CWEs, as well as CVEs with no risk score, are displayed with the standard size 20. 

*graph.png*: sample output of the program (saved as matplotlib figure and then converted to .png file) 

Potential Improvements:
 * JSON to CSV or Pandas Dataframe Conversion 
 * Handling Large Datasets: Clean visualization with networkx is difficult when using large datasets
 * Labeling: The text box specifying label details might need to be replaced by clearer labels under each node
 * Node Size Customization: There might be a more direct way to achieve this 
