# test for quantiNemo

This repository contain a set of test for quantiNemo 2. 
Since covering the entire code of qN with unitary test was out of the scope of this project, we developed more something like end-user functional test. 
The test cover mainly the new features of quantiNemo 2 and basics feature of quantiNemo 1. 
Covering all parameters, a fortiori all interaction between parameters, would be a very long task and the test are not attended to do so for now. 
If people take-on the development of qN, they are encouraged to keep developing this set of tests.

we came across two main challenges while developing them. 
Since qN has a stochastic component, a given input produce different outputs. This mean that most test are actually statistical test. 
It is then difficult to find the right balance between computational time, statistic power and false failure. On solution is to seed the test, but this has also some drawback.
If we were to restart this from the beginning, one option would be to develop two set of tests. One of them with little power and seed which could run quickly (seconds to 1 minutes),
and another set without seed, with more statistical power which would run in a matter of hours. 

## Getting Started

To run all tests, the notebook test_all.Rmd can be used. All test can also be run individually by opening the related notebook. 

These test use RquantiNemo, a package to use quantiNemo within R. 
Currently (and it is so because RQuantiNemo was never completely finished), a copy of RquantiNemo should be present in a parent directory. 
The version of quantiNemo being tested is the one present in the RquantiNemo rep. 



