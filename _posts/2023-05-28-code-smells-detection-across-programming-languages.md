---
layout: post
title:  "TSE: Code Smells Detection Across Programming Languages"
categories: code-smells
---

# Resume

The incidence of code smells is often associated with software quality degradation. Several studies present the importance of techniques to detect and tackle the incidence of smells in the source code. However, existing techniques to detect code smells depend on the programming language. Consequently, several programming languages are largely employed by the software community without proper techniques of code smell detection. Our study addresses amplifying the availability of code smell detection techniques to different programming languages through transfer learning. We select five programming languages among the ten most used languages according to StackOverflow: Java, C++, Python, C#, and JavaScript. We extract the datasets for training and testing of deep learning models from 150 open sources projects. Results indicate that transfer learning techniques effectively and efficiently detect code smells regardless of the programming language and complexity of the deep learning architecture used in transfer learning. These findings can help developers and researchers to apply the same code smell detection techniques in different programming languages. 

# Code Smells - Detection Rules


| Code Smell       | Programming Languages                | Rule                                                      |
|------------------|--------------------------------------|-----------------------------------------------------------|
| Complex Method   | Java, C#, C++, JavaScript and Python | CC >= 8                                                   |
| Long Method      | Java, C#, C++ and Python             | (LOC > 50) and (CC > 5)                                   |
| Shotgun Surgery  | Java, C# and C++                     | (CC > 4) and (FanOut > 7)                                 |
| Feature Envy     | Java, C# and C++                     | (CC > 4) and (FanOut > 4) and (LCOM textless 30%)         |
| Divergent Change | Java, C# and C++                     | (FanIn > 10) and (LCOM textless 50%) and (CC > 4)         |
| God Class        | Java, C#, C++ and Python             | [(LOC > 150) and (CBO > 6)] or [(NOM > 15) and (CBO > 6)] |
