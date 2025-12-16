# README

## 1. Data
| Filename       | Dataset Description                                                                 | Data Volume | Additional Parameters                          |
|----------------|-------------------------------------------------------------------------------------|-------------|------------------------------------------------|
| Stock.txt      | Bitcoin Stock Price Dataset                                                        | 9,028,997   | -                                              |
| Power.txt      | UK Electricity Dataset                                                            | 246,284     | -                                              |
| Genome.txt     | Scoring sequences derived from the *Haemophilus influenzae* genome                 | 1,837,622   | -                                              |
| Uniform.txt    | Generated dataset following a uniform distribution                                | 1,000,000   | Uniform distribution with Min=-1000, Max=1000   |
| Normal.txt     | Generated dataset following a normal distribution                                 | 1,000,000   | Normal distribution with Mean=0, Std=1000       |


## 2. Algorithm Code
The algorithm code is divided into two parts, corresponding to different experimental scenarios in the paper:

### 2.1 Code for Overall and Throughput Experiments
The following C++ source files correspond to the five algorithms mentioned in the paper, used for Overall and Throughput experiments:
- `Overall_Throughput_Partition.cpp`
- `Overall_Throughput_Streaming_RT.cpp`
- `Overall_Throughput_Streaming_Tournament.cpp`
- `Overall_Throughput_RuzzoTompa.cpp`
- `Overall_Throughput_Tournament.cpp`

### 2.2 Code for Memory and Candidate Experiments
The following C++ source files are used for Memory and Candidate experiments. Note that the Tournament and Streaming_Tournament algorithms do not involve the concept of "Candidate" and thus are not included in Candidate experiments:
- `Memory_Candidate_Partition.cpp`
- `Memory_Candidate_RuzzoTompa.cpp`
- `Memory_Candidate_Streaming_RT.cpp`
- `Memory_Streaming_Tournament.cpp` (Only for Memory experiment)
- `Memory_Tournament.cpp` (Only for Memory experiment)


## 3. Python Scripts for Invoking Algorithm Code
Python scripts are categorized into three types, which can be run directly to save experimental results into corresponding txt files:

### 3.1 Scripts for Overall Experiments
- `Invoke_Overall_Partition.py`
- `Invoke_Overall_Streaming_RT.py`
- `Invoke_Overall_Streaming_Tournament.py`
- `Invoke_Overall_RuzzoTompa.py`
- `Invoke_Overall_Tournament.py`

### 3.2 Scripts for Throughput Experiments
These scripts generate results of the five algorithms under different parameters:
- `Invoke_Throughput_Partition.py`
- `Invoke_Throughput_Streaming_RT.py`
- `Invoke_Throughput_Streaming_Tournament.py`
- `Invoke_Throughput_RuzzoTompa.py`
- `Invoke_Throughput_Tournament.py`

### 3.3 Scripts for Memory and Candidate Experiments
These scripts generate results of the five algorithms under different parameters. The Tournament and Streaming_Tournament algorithms only output Memory experiment results:
- `Invoke_Memory_Candidate_Partition.py`
- `Invoke_Memory_Candidate_Streaming_RT.py`
- `Invoke_Memory_Tournament.py`
- `Invoke_Memory_Candidate_RuzzoTompa.py`
- `Invoke_Memory_Tournament.py`

### Note
- All "Throughput" uses the standard spelling for the experimental metric (throughput).
- All scripts output experimental results to txt files with corresponding names (e.g., `Invoke_Overall_Partition_results.txt`), which are automatically generated in the same directory after running the scripts.