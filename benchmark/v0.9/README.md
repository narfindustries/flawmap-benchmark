# CVE AI Flaw Mapper Benchmark 

Version 0.9: Studious Gargoyle

This is the list of CVEs used to run our analysis for the research paper. 
The list is in the file `cvelist-studious-gargoyle.json` in this directory.

This list results in our UPxi SSAs correctly identifying just over 62% of the true positive CVEs.

# Description

The list of CVEs is drawn from the NVD CVE list maintained at `https://github.com/CVEProject/cvelistV5`

The contents of this list are the complete set of CVEs selected to admit to the front of our processing pipeline.

This pipeline is a two-stage process. First, we run the FlawMapper tool to attempt to map from the CVE description 
and repository information back to the actual _culprit commit_ that introduced the flaw.  The FlawMapper is a very
strict filter that passes a small fraction of the larger test set. We are investigating ways to harvest more of the
resolved mappings. The second step is to take the resolved list and apply our AI/LLM Agents to the identified commits.
The Agents do not have any prior information about whether that commit contains a flaw or vulnerability. Since the
commit is a True Positive, they (and others like them) should identify the specific flaw (not just the general high
level fact that there may be a security flaw in that commit).

These projects contain 7 common source code languages and 16 other assorted languages.

The CVEs cover more than 20 CWE types.

# Results

```
N = 896
Number of CVEs Resolved by FlawMapper = 134
Number of additional likely but discarded resolutions = 115

Source Security Agents subselection = 103 (out of 134)
Source Security Agents identification count = 64
Source Security Agents success rate = 62% (64/103)
```

# Background Material

TBD.
