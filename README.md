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
# Q62. Write a covergroup to sample a 3-bit opcode with:
       Individual bins for opcodes 0, 1, 2
       Illegal bin for opcode 7
# Q63. Implement a covergroup that samples only when enable is high.
# Q64. Write a covergroup to cross two signals:
       cmd (READ, WRITE)
       addr (LOW: 0x0-0xFF, HIGH: 0x100-0x1FF)
# Q65. How to reduce cross coverage bins between two 4-bit signals? (Use ignore_bins or binsof)
# Q66. Write a coverpoint to check transitions:
       0 → 1 → 2
       1 → 3 → 5
# Q67. How to cover a scenario where signalA is high, and within 3 cycles, signalB is high? Use a sequence and sample it in coverage.
# Q68. Cover a 32-bit address space with:
       First 1KB (0x0000-0x03FF)
       Last 1KB (0xFC00-0xFFFF)
       All other addresses as a single bin
# Q69. How to cover only even values of a 16-bit counter?
# Q70. Write a covergroup where bins are dynamically enabled based on a configuration register.
# Q71. How to implement "coverage per test" (merge coverage only for specific tests)?
# Q72. Cover only the cases where cmd == READ and status == OK.
# Q73. How to exclude addr == 0xDEADBEEF from all crosses?
# Q74. Write a covergroup to measure how many times a FIFO goes from empty to full in a single test.
# Q75. Cover all possible burst lengths (1, 2, 4, 8) and burst types (INCR, WRAP) in an AXI transaction.
# Q76. Implement coverage for a state machine with 3 states (IDLE, ACTIVE, ERROR) and all transitions.
# Q77. Write a SystemVerilog covergroup to monitor APB read and write transactions, including:
       PWRITE (direction)
       PADDR range (split into 4 equal bins)
       PWDATA and PRDATA values (8-bit, with all-ones and all-zeros bins)
# Q78. Write a covergroup to track APB state transitions (IDLE → SETUP → ACCESS → IDLE)
# Q79. Write a covergroup to track how many cycles PREADY takes to respond (0-cycle, 1-cycle, 2-5 cycles, >5 cycles) in APB.
# Q80. Write a covergroup to ensure PSLVERR is tested under different conditions in APB:
       During reads vs. writes
       With different PADDR ranges
       After different PREADY delays
# Q81. How would you write a covergroup to detect if multiple PSELx signals are accidentally asserted at the same time in APB?
# Q82. How would you modify the covergroup to ensure APB transactions are verified during power transitions (e.g., clock gating, reset)?
# Q83. Write a covergroup to track back-to-back APB transactions (no idle cycle between them)
# Q84. Write a covergroup to ensure that after a PSLVERR, the next transaction is successful (PREADY with no error) in APB.
# Q85. How would you write a covergroup to track unaligned 32-bit APB accesses (where PADDR[1:0] != 2'b00)?
# Q86. Write a covergroup to track how many cycles PREADY stays low (stall duration).
# Q87. Write a covergroup to check if the APB bus resumes transactions correctly after reset.
# Q88. Write a covergroup to ensure that a read after write to the same address returns the previously written data.
# Q89. How would you write a covergroup to track APB transactions triggered by peripheral interrupts (assume an interrupt signal IRQ)?
# Q90. Write a covergroup to categorize APB transfers into:
       Single read
       Single write
       Back-to-back read after write
       Back-to-back write after read
# Q91. Cover cases where PADDR falls into unmapped regions (address holes). Assume valid range is 0x0000–0x0FFF.
# Q92. Cover PSTRB usage in APB4 for partial writes (e.g., byte-wise writes).
# Q93. Cover illegal transitions (e.g., PENABLE without PSEL, or PREADY before PENABLE) in APB
# Q94. Cover the first transaction after reset de-assertion in APB.
# Q95. Cover all combinations of PREADY and PSLVERR responses in APB.
# Q96. Cover scenarios where multiple slaves are accessed in rapid succession in APB.
# Q97. Cover cases where PRDATA changes while PREADY is low in APB
# Q98. Cover APB transactions that occur during clock gating scenarios
# Q99. Cover the  APB initialization sequence where a peripheral is configured after reset.
# Q100. Write a covergroup to track AXI read and write bursts (INCR, WRAP, FIXED) and their lengths (1, 2, 4, 8, 16 beats).
# Q101. Cover the number of outstanding transactions (0-8) on a channel (e.g., read or write) in AXI.
# Q102. Cover interleaved write data (WID changes mid-burst) in AXI.
# Q103. Cover all AXI response types (OKAY, EXOKAY, SLVERR, DECERR) in AXI.
# Q104. Cover atomic operations (e.g., exclusive accesses, SWAP, CAS) in AXI.
# Q105. Cover cases where read data returns out-of-order (BID/RID ≠ FIFO order) in AXI.
# Q106. Cover partial writes using WSTRB (e.g., byte-wise, half-word) in AXI.
# Q107. Cover transactions during clock gating or power state changes in AXI.
# Q108. Cover bufferable (AxCACHE) vs. non-bufferable transactions in AXI.
# Q109. Cover unaligned burst starts (e.g., 4-byte burst starting at 0x3) in AXI.
# Q110. Write FC Code to Track maximum outstanding transactions per ID in AXI.
# Q111. Cover interleaving depth (number of concurrent WID values) in AXI.
# Q112. Write FC code to Cover exclusive access success vs. failure cases in AXI.
# Q113. Write FC code to Cover different WDATA arrival patterns relative to AW in AXI.
# Q114. Write FC code to Cover cacheable vs. non-cacheable transactions(AXI Cache Coherency Scenarios).
# Q115. Write FC code to Cover OOO completion by RID/BID (AXI Out-of-Order Completion Patterns).
# Q116. Write FC code to Cover transactions during power state changes.
# Q117. Write FC code to Cover partial strobes with all-0/all-1 data (AXI Write Strobe Edge Cases)
# Q118. Write FC code to Cover deliberate error injection cases (AXI Error Injection Coverage).
# Q119. Write FC code to Cover transactions crossing 4KB boundaries (AXI Byte Lane Crossing).
# Q120. Write FC code to Cover CDC scenarios for multi-clock AXI (AXI Clock Domain Crossing).
# Q121. Write FC code to Cover basic FIFO operations (Synch FIFO write, read, simultaneous write-read).
# Q122. Write FC code to Cover Synch FIFO fill states (empty, half-full, full)
# Q123. Write FC code to Cover transitions between full and empty states in Synch FIFO.
# Q124. Write FC code to Cover illegal overflow (write when full) and underflow (read when empty) in Synch FIFO.
# Q125. Write FC code to Verify data correctness after write-read sequences in Synch FIFO.
# Q126. Write FC code to Cover Synch FIFO behavior post-reset (first write after reset).
# Q127. Write FC code to Cover back-to-back write-read patterns ( Synch FIFO Concurrent Read/Write Stress)
# Q128. Write FC code to Cover write/read pointer wrap-around cases (Synch FIFO Pointer Wrap-Around).
# Q129. Write FC code to Cover programmable almost-full/almost-empty thresholds (FIFO Threshold Triggers).
# Q130. Write FC code to Cover read-after-reset to ensure no stale data (FIFO Power-On Reset Data).
# Q131. Write FC code to Cover full→empty→full stress sequence in Synch FIFO.
# Q132. Write FC code to Cover reset during active read/write operations in Synch FIFO.
# Q133. Write FC code to Cover cases where write and read occur simultaneously at empty/full boundaries (FIFO Simultaneous Push-Pop at Boundaries).
# Q134. Write FC code to Verify data integrity after consecutive writes followed by reads (FIFO Data Retention After Multiple Writes).
# Q135. Write FC code to Cover cases where write and read pointers collide (not just full/empty, FIFO Pointer Collision ).
# Q136. Write FC code to Cover transitions of almost-full/almost-empty flags (FIFO Almost-Full/Almost-Empty Toggle).
# Q137. Write FC code to Cover complete fill-then-drain sequences (FIFO Sequential Fill-Drain Patterns).
# Q138. Write FC code to Cover maximum throughput scenarios (every cycle write-read,FIFO High-Frequency Write-Read)
# Q139. Write FC code to Cover interrupted write/read sequences (FIFO Partial Write-Read Sequences).
# Q140. Write FC code to Cover reset while FIFO is full (stress case,FIFO Reset During Full Operation).
# Q141. Write FC code to Cover basic write (wr_clk domain) and read (rd_clk domain) operations in Asynch FIFO (Basic Async FIFO Operations).
# Q142  Write FC code to Cover transitions of empty/full flags synchronized across domains (FIFO Empty/Full Flags (CDC-Safe) Cover) in Asynch FIFO.
# Q143. Write FC code to Cover FIFO fill levels (empty, half-full, full) using Gray-coded pointers (FIFO Fill Levels (Gray Code Conversion)) in Asynch FIFO.
# Q144. Write FC code to Verify all valid single-bit Gray code transitions for write/read pointers (Gray Code Pointer Transitions (CDC Critical!)) in Asynch FIFO.
# Q145. Write FC code to Cover cases where synchronized pointers recover from metastability (Metastability Recovery Coverage) in Asynch FIFO.
# Q146. Write FC code to Cover different clock frequency ratios (e.g., wr_clk 2x faster than rd_clk) (Write-Read Clock Frequency Ratios) in Asynch FIFO.
# Q147. Write FC code to Cover illegal writes when full (wr_clk domain) and reads when empty (rd_clk domain). (FIFO Overflow/Underflow (CDC-Safe)) in Asynch FIFO.
# Q148. Write FC code to Cover synchronization delay for pointers crossing clock domains (Pointer Synchronization Latency) in Asynch FIFO.
# Q149. Write FC code to Cover burst writes followed by burst reads with different clock ratios (Back-to-Burst Write-Read) in Asynch FIFO.
# Q150. Write FC code to Cover reset deassertion in both clock domains .( FIFO Reset Recovery (Dual-Clock)) in Asynch FIFO.
# Q151. Write FC code to Cover full-to-empty-to-full transitions across clock domains (Full→Empty→Full Transition (CDC)) in Asynch FIFO.
# Q152. Write FC code to Cover pointer drift when one clock is much faster than the other (Pointer Drift Under Extreme Clock Skew) in Asynch FIFO.
# Q153. Write FC code to Verify data correctness after crossing clock domains (Data Integrity After CDC) in Asynch FIFO.
# Q154.
# Q155.
# Q156.
# Q157.
# Q158.
# Q159.
# Q160.
# Q161.
# Q162.
# Q163.
# Q164.
# Q165.
# Q166.
# Q167.
# Q168.
# Q169.
# Q170.
# Q171.
# Q172.
# Q173.
# Q174.
# Q175.
# Q176.
# Q177.
# Q178.
# Q179.
# Q180.
# Q181.


