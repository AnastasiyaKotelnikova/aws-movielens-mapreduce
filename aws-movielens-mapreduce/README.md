AWS MovieLens MapReduce Project
This project demonstrates the setup and execution of a Hadoop MapReduce job on AWS EC2 instances using the MovieLens dataset. It was completed as part of the Big Data course at NJIT.

Project Overview
We deployed a two-node Hadoop cluster (Master + Slave) on AWS EC2 and executed a MapReduce job to identify the most rated movies from the MovieLens dataset using custom Java classes.

AWS Infrastructure Setup
EC2 Master and Slave instances launched (t3.medium)
Passphraseless SSH configured for Hadoop cluster communication
Hadoop installed and configured
Java MapReduce job compiled and executed
Dataset
Name: MovieLens 1M
Source: GroupLens
Format: .dat file (tab-separated)
Size: ~5MB
Reason for Use: Ideal for demonstrating distributed movie rating analysis
Project Structure
aws-movielens-mapreduce/
├── BigData_Option1_Kotelnikova_Anastasiya.docx     # Milestone 1 report
├── BigData_Option1_Kotelnikova_Anastasiya_Milestone2.docx # Milestone 2 report
├── Screenshots/                                   # All EC2 & Hadoop CLI screenshots
│   ├── AWS EC2 Master & Slave Instances Running.png
│   ├── Passphraseless SSH Login Screenshots.png
│   ├── JPS Output on Master and Slave Nodes.png
│   ├── Screenshot 1: Running the job command.png
│   ├── Screenshot 2.1 & 2.2: Process of MapReduce.png
│   └── Screenshot 3: Output results from HDFS.png
├── README.md                                      # Project overview

---

## Key Concepts

- EC2 instance management and SSH setup
- Hadoop HDFS initialization and formatting
- Java-based MapReduce job with custom Mapper and Reducer
- Running and monitoring MapReduce jobs on a real cluster

---

## Output Sample

```bash
hdfs dfs -cat /output/part-r-00000
1193    1
661     1
914     1

---

## Output Summary

The program successfully completed all MapReduce phases without error:

- Map 100% | Reduce 100%
- Status: `Job completed successfully`
- Output file contains movie IDs with their respective rating counts

---

## Challenges & Learnings

- Faced SSH connection issues due to firewall/port settings — resolved by updating security group rules on EC2
- Understood how to format namenodes and start daemons using `start-dfs.sh` and `jps`
- Learned how to compile and run custom MapReduce jobs using `hadoop jar`

---

## Author

**Anastasiya Kotelnikova**  
Master’s Student in Data Science at NJIT  
Email: [anastasiya.kotelnikova21@gmail.com](mailto:anastasiya.kotelnikova21@gmail.com)

