# *****************************
# Functional_Coverage_Coding_by_Siba
# 👯 Acknowledgments : System Verilog community members , Open Source resources and Verification experts who have helped a lot in guiding me.
# 🤔 Encouragement   : Don't forget to star this repository if you find it helpful throughout your learning !!!
# ⚡ GitHub Repo     : https://github.com/Sibakumarpanda/Functional_Coverage_Coding_by_Siba/
# *****************************
# -------->  Problem Sets for Practice <-------
# Q1. Write FC code to demonstrate randomization and coverage collection using a class my_packet with addr and data fields and a covergroup cg to monitor these fields during simulation. Perform running 20 random tests and samples the coverage.
# Q2. What is functional coverage and How does functional coverage differ from code coverage?
# Q3. What are coverage points?
# Q4. How do you define a coverage model in SystemVerilog ?
# Q5. What is a covergroup, and how is it used?
# Q6. Explain the difference between coverpoints and cross coverage.
# Q7. How do you handle functional coverage for a design with multiple configurations?
# Q8. What strategies do you use to achieve 100% functional coverage?
# Q9. How do you analyze and interpret coverage reports?
# Q10. What is coverage closure and how do you achieve it?
# Q11. How do you integrate functional coverage with constrained random verification?
# Q12. Can you provide an example of a covergroup definition in SystemVerilog?
# Q13. How do you use coverage data to improve your verification environment?
# Q14. What are bins in the context of functional coverage?
# Q15. How do you decide which functional coverage points to include in your coverage model?
# Q16. How do you handle coverage for asynchronous signals or events?
# Q17. What is the role of coverage exclusion, and how do you implement it?
# Q18. How do you use functional coverage to guide test generation?
# Q19. What challenges have you faced in achieving coverage closure, and how did you overcome them?
# Q20. How do you balance between achieving high functional coverage and simulation performance?
# Q21. How do you integrate functional coverage with formal verification techniques?
# Q22. How would you handle functional coverage for a design with dynamically changing configurations?
# Q23. Explain how you would use functional coverage to verify a design with multiple clock domains.
# Q24. How can you ensure that rare corner cases are covered in a design with a large state space?
# Q25. How do you handle coverage points that are consistently missed despite extensive testing?
# Q26. Write a covergroup to track the values of a 4-bit counter. Ensure that all possible values are covered.
# Q26. Implement a covergroup to check cross coverage between two signals: mode (3-bit) and status (2-bit).
# Q27. How would you modify a covergroup to exclude certain values from being covered? Provide an example.
# Q28. Write a covergroup to track the transitions of a state machine with states IDLE, RUN, and STOP
# Q29. How would you parameterize a covergroup to handle different signal widths? Provide an example.
# Q30. Write a covergroup to track the occurrence of specific events, such as a signal going high.
# Q31. How would you implement conditional coverage to only track values when a valid signal is high ?
# Q32. Explain the key components of functional coverage (covergroups, coverpoints, bins, crosses).
# Q33. What is the difference between auto bins and user-defined bins?
# Q34. What happens if no bins are explicitly defined for a coverpoint?
# Q35. How do you ignore or exclude certain values from coverage?
# Q36. What is an illegal_bin, and how is it used?
# Q37. How do you handle transitions in functional coverage (e.g., 0 -> 1 -> 2)?
# Q38. What is the impact of crossing two 8-bit variables without bin reduction?
# Q39. How can you exclude certain cross combinations?
# Q40. How do you trigger coverage sampling (e.g., using sample() method)?
# Q41. What are the different weight, goal, and at_least options in coverage?
# Q42. How do you merge coverage from multiple test runs?
# Q43. What is the difference between per_instance and per_type coverage?
# Q44. How do you analyze coverage holes?
# Q45. How would you cover a scenario where a signal should never take a specific value?
# Q46. How do you define bins for a multi-bit signal where only certain bit patterns are interesting?
# Q47. How would you cover a scenario where a 32-bit address should cover ranges (e.g., 0x0000-0x0FFF, 0x1000-0x1FFF)?
# Q48. How do you handle coverage for a signal that can take millions of possible values (e.g., a 64-bit counter)?
# Q49. What happens if you cross two coverpoints, one with 4 bins and another with 5 bins? How many bins are created?
# Q50. How can you avoid exponential bin explosion in cross coverage?
# Q51. How would you cover all possible 2-bit transitions (e.g., 00→01→10→11)?
# Q52. How do you enable/disable coverage sampling based on a condition?
# Q53. How can you dynamically modify bins during simulation?
# Q54. How would you implement temporal coverage (e.g., Signal A high → within 5 cycles → Signal B high)?
# Q55. If coverage is not reaching 100%, how would you debug the issue?
# Q56. How can you prioritize coverage holes to focus on the most critical ones?
# Q57. What is covergroup strobe sampling, and when would you use it?
# Q58. Scenario: A FIFO has full, empty, and almost_full conditions. How would you cover all possible state transitions?
# Q59. Scenario: A register field can be READ-ONLY, WRITE-ONLY, or READ-WRITE. How would you ensure all access modes are covered?
# Q60. Scenario: A state machine has 5 states. How would you ensure all transitions are covered?
# Q61. Write a covergroup to cover an 8-bit data bus with bins for:
       Values 0, 1, 2
       Range 100 to 200
       All other values (auto bins)
# Q62.
# Q63.
# Q64.
# Q65.
# Q66.
# Q67.
# Q68.
# Q69.
# Q70.
# Q71.
# Q72.
# Q73.
# Q74.
# Q75.
# Q76.
# Q77.
# Q78.
# Q79.
# Q80.
# Q81.
# Q82.
# Q83.
# Q84.
# Q85.
# Q86.
# Q87.
# Q88.
# Q89.
# Q90.

