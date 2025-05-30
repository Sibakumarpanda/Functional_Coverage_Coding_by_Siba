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
# Q154. Write FC code to Cover all Transaction Layer Packet (TLP) types (Memory Read/Write, I/O, Configuration, Completion) in PCIe. (PCIe Transaction Types (TLP Types))
# Q155. Write FC code to Cover different address ranges (e.g., MMIO, I/O, Configuration Space) in PCIe. (PCIe Address Ranges)
# Q156. Write FC code to Cover all Completion Status codes (Successful, Unsupported Request, Completer Abort) in PCIe. (PCIe Completion Status)
# Q157. Write FC code to Cover different TLP payload sizes (1DW, 2DW, max payload) in PCIe.(PCIe Payload Sizes)
# Q158. Write FC code to Cover flow control credit updates (PH, PD, NPH, NPD) in PCIe. (PCIe Flow Control Credits)
# Q159. Write FC code to Cover AtomicOp TLPs (FetchAdd, Swap, CAS) in PCIe. (PCIe Atomic Operations)
# Q160. Write FC code to Cover completions with mismatched Tag/Requester ID in PCIe. (PCIe Unexpected Completions)
# Q161. Write FC code to Cover different Max Read Request Sizes (128B, 256B, 512B, 1024B) in PCIe. (PCIe Max Read Request Size (MRRS))
# Q162. Write FC code to Cover TLP with Maximum Payload Size (e.g., 1024 bytes),Misaligned Addresses, Cross 4KB Boundary Splits in PCIe. (Large Payload & Address Alignment) 
# Q163. Write FC code to Cover illegal TLP formats (e.g., wrong Fmt/Type combinations) in PCIe. (PCIe Malformed TLP Detection)
# Q164. Write FC code to Cover all valid combinations of TLP Formats (Fmt) and Types in PCIe. (TLP Type & Format Coverage)
# Q165. Write FC code to Cover PCIe error scenarios like Unsupported Requests (UR), Completer Abort (CA), Poisoned TLPs,ECRC Errors etc.
# Q166. Write FC code to Cover correctable/uncorrectable error triggers in PCIe. (PCIe AER (Advanced Error Reporting))
# Q167. Write FC code to Cover transactions targeting different functions (FN 0-7) in PCIe. (PCIe Multi-Function Devices)
# Q168. Write FC code to Cover dynamic BAR resizing operations in PCIe. (PCIe Resizable BAR (rBAR))
# Q169. Write FC code to Cover AtomicOp completion data integrity in PCIe. (AtomicOp Completer Handling)
# Q170. Write FC code to Cover unaligned addresses and lengths for Memory TLPs in PCIe. (Address/Length Alignment)
# Q171. Write FC code to Cover all possible Tag values (0-255) per Requester ID in PCIe. (Tag Usage)
# Q172. Write FC code to Cover illegal TLP combinations (e.g., Completion with Length≠1) in PCIe. (Malformed TLP Detection)
# Q173. Write FC code to Cover TLP Digest (ECRC) enabled/disabled cases in PCIe. (TLP Digest (ECRC/EDCRC))
# Q174. Write FC code to Cover out-of-order completion handling in PCIe. (TLP Processing Order)
# Q175. Write FC code to Cover VC arbitration for different TLP classes (Posted/Non-Posted) in PCIe. (Virtual Channel Arbitration)
# Q176. Write FC code to Cover TPH (TLP Processing Hint) and other prefixes in PCIe. (TLP Prefixes (PCIe 5.0+))
# Q177. Write FC code to Cover MRRS settings impact on Read TLPs in PCIe. (Max Read Request Size (MRRS))
# Q178. Write FC code to Cover completion timeout scenarios in PCIe. (Completion Timeout)
# Q179. Write FC code to Cover unexpected link down events in PCIe. (PCIe Surprise Down (Advanced Error Handling))
# Q180. Write FC code to Cover link training states (LTSSM: L0, Recovery, Disabled) in PCIe. (PCIe Link Training & Recovery)
# Q181. Write FC code to Cover transitions between power states in PCIe. (PCIe Power Management (L1/L2/L3))
# Q182. Write functional coverage code to include entry/exit conditions for Electrical Idle (EI) in PCIe physical layer.
# Q183. Write FC code to check Receiver Detection (Rx Detect) properly verified when exiting Electrical Idle in PCIe.
# Q184. Write FC code to check L0, L0s, L1, L2, L3 power states exercised with correct transitions in PCIe.
# Q185. Write FC code to check LTSSM State Transitions in PCIe.
# Q186. Write FC code to include Recvery due to errors (e.g. SKP OS mismatch, 8b/10b disparity) in PCIe?
# Q187. Write FC code to check Link Width Configuration & Lane Negotiation in PCIe.
# Q188. Write FC code to check coverage for lane reversal and polarity inversion cases in PCIe.
# Q189. Write FC code to check Speed Negotiation/Speed Change with Maximum Supported Speed of GEN5 in PCIe.
# Q190. Write FC code to cover SSC (Spread Spectrum Clocking) impact on speed negotiation in PCIe.
# Q191. Write FC code to cover Power State Transitions in PCIe.
# Q192. Write FC code to add coverage for Electrical Idle exit sequences (EIOS handling) in PCIe.
# Q193. Write FC code to cover Error Handling & Recovery Coverage in PCIe (Error-Induced Recovery, the error may be due to: skp_mismatch,disparity_error,crc_error)
# Q194. Write FC code to include multiple retries before successful recovery?
# Q195. Write FC code for EQ Preset and Margining(Voltage/Time) in PCIe.
# Q196. Write FC code to track successful vs. failed equalization attempts in PCIe.
# Q197. Write FC code for Reset & Initialization Coverage in PCIe.
# Q198. Write FC code for Partial vs. Full Link Re-initialization after reset in PCIe.
# Q199. Write FC code for Compliance Pattern Testing in Gen5 PCIe.
# Q200. Write FC code for Deskew & Lane-to-Lane Skew Compensation in PCIe.
# Q201. Write FC code to add coverage for multi-lane deskew sequences (x4, x8, x16) in PCIe.
# Q202. Write FC code to check L0s/L1 Entry-Exit Timing (Power State Entry/Exit Latency) in PCIe.
# Q203. Write FC code to check unexpected wakeups (e.g., Beacon signaling) during L1 in PCIe.
# Q204. Write FC code to check EQ Phase 1/2/3 Success in Gen5 PCIe.
# Q205. Write FC code to add coverage for fallback to lower-gen speeds if EQ fails , in PCIe.
# Q206. Write FC code to cover Error Injection Scenarios (INVALID_8B10B,DISPARITY_ERROR,DLLP_CRC_ERR) in PCIe.
# Q207. Write FC code to cover multiple consecutive errors (e.g., 3 CRC errors in a row) in PCIe.
# Q208. Write FC code to add coverage for PERST# assertion duration (100ms vs. 1ms) in PCIe.
# Q209. Write FC code to check for Lane Drop/Readd Events (Multi-Lane Link Stability) in PCIe.
# Q210. Write FC code to cover dynamic lane width reduction (e.g., x8 → x4 due to errors) in PCIe.
# Q211. Write FC code to validate compliance patterns in PCIe Gen4, Gen5 Loopback scenarios.
# Q212. Write FC code to check Successful Speed Upgrades in PCIe. (Basic Speed Negotiation :Gen1 → Gen2 → Gen3 → Gen4 → Gen5)
# Q213. Write FC code to cover down-negotiation (e.g., Gen4 → Gen3) due to signal integrity issues in PCIe.
# Q214. Write FC code to cover Speed Fallback Due to Errors in PCIe. (Error-Induced Speed Fallback: Mean for example while in Gen3, it will go to its previous speed that is Gen2 )
# Q215. Write FC code to check Recovery After Speed Change in PCIe (LTSSM State During Speed Change).
# Q216. Write FC code to check SSC (Spread Spectrum Clocking) Impact on Speed Stability in PCIe.
# Q217. Write FC code to cover EQ preset changes when switching speeds (e.g., Gen3 → Gen4) in PCIe.
# Q218. Write FC code to cover Speed Change with Data Transmission (Speed Change During Active Traffic)
# Q219. Write FC code to track TLP retries due to speed-change-induced packet loss in PCIe.
# Q220. Write FC code to check Beacon Wakeup to New Speed in PCIe. (Beacon-Triggered Speed Re-Negotiation)
# Q221. Write FC code to check Speed After Hot Reset in PCIe . (Hot Reset with Speed Change)
# Q222. Write FC code to verify forced downgrades after Hot Reset due to errors in PCIe.
# Q223. Write FC code to verify Speed After Link Retraining in PCIe .(Link Up/Down Speed Stability).
# Q224. Write FC code to track maximum retries before link drops in PCIe.
# Q225. Write FC code to cover exit from compliance mode to negotiated speed in PCIe.
# Q226. Write FC code to cover Random Speed Change During Active Link in PCIe (Ad-Hoc Speed Transition).
# Q227. Write FC code to cover unexpected speed changes during max payload transmission in PCIe.
# Q228. Write FC code to check LTSSM State Transitions During Speed Change in PCIe (LTSSM Behavior During Random Speed Changes)
# Q229. Write FC code to track time spent in Recovery for each speed transition in PCIe.
# Q230. Write FC code to check Speed Change Failures in PCIe.(Error Handling During Random Speed Changes).
# Q231. Write FC code to check Clock Behavior During Speed Changes in PCIe. (Clock Stability Post-Speed Change)
# Q232. Write FC code to check Lane-Specific Speed Changes in PCIe.(Multi-Lane Speed Alignment)
# Q233. Write FC code to cover lane-to-lane speed mismatches during transitions in PCIe.
# Q234. Write FC code to cover Speed Change Stress Test scenario in PCIe. (Consecutive Speed Changes)
# Q235. Write FC code to track link stability after 5+ consecutive speed changes in PCIe
# Q236. Write FC code to track Speed Change with DLLP/TLP Traffic in PCIe. (Packet Loss During Speed Change)
# Q237. Write FC code to cover Forced Speed in Compliance Mode in PCIe, ensuring compliance mode doesn’t corrupt negotiated speed. (Compliance Mode vs. Negotiated Speed)
# Q238. Write FC code to cover Basic Link Width Negotiation in PCIe . (X1,X2, X4,X8, X16)
# Q239. Write FC code to cover lane reversal and polarity inversion during initial negotiation in PCIe.
# Q240. Write FC code to cover Dynamic Link Width Reduction (e.g., x8 → x4, X16->X8)) in PCIe. (Active Width Downgrade)
# Q241. Write FC code to track TLP/DLLP retransmissions during link width reduction in PCIe.
# Q242. Write FC code to cover Link Width Recovery Upsizing and Downsizing in PCIe .(Example : LINK_WIDTH_X4 ->LINK_WIDTH_X8 or LINK_WIDTH_X8 ->LINK_WIDTH_X4 )
# Q243. Write FC code to cover failed recovery attempts (e.g., x4 → x8 fails due to noise) in PCIe.
# Q244. Write FC code to cover LTSSM Transitions for Link Width Reconfiguration in PCIe. (LTSSM State During Width Change)
# Q245. Write FC code to measure time spent in CONFIG_LINKWIDTH state during width changes in PCIe
# Q246. Write FC code to track Lane Deskew After Width Change in PCIe. (To detect lane-to-lane skew violations after width changes)
# Q247. Write FC code to track Error Handling During Width Change .(Errors Triggering Width Reduction)
# Q248. Write FC code to cover multiple lane failures (e.g., 2 lanes drop in x8) in PCIe.
# Q249. Write FC code to cover Link Width Changes During L1/L0s ltssm state transition in PCIe.
# Q250. Write FC code to track unexpected width changes during Electrical Idle in PCIe.
# Q251. Write FC code to cover Hot Reset and Link Width scenario. (Post-Reset Width Re-Negotiation)
# Q252. Write FC code to cover  forced width reduction after Hot Reset in PCIe.
# Q253. Write FC code to cover Consecutive Width Changes scenarios in PCIe. (Multi-Lane Stability Stress Test)
# Q254. Write FC code to track link stability after 10+ consecutive width changes in PCIe.
# Q255. Write FC code to check Simultaneous Speed + Width Change in PCIe (Coordinated Speed and Width Transition).
# Q256. Write FC code to cover Speed Upgrade with Width Downgrade scenario in PCIe.(Speed↑ + Width↓ Tradeoff)
# Q257. Write FC code to cover Speed Downgrade with Width Upgrade scenario in PCIe.(Speed↓ + Width↑ Tradeoff)
# Q258. Write FC code to cover Surprise Removal/Insertion scenario in PCIe . (Hot Plug with Speed+Width Re-negotiation)
# Q259. Write FC code to cover Rapid/Back-to-back Speed+Width Changes in PCIe . (Consecutive Reconfigs, Stress Testing ) 
# Q260. Write FC code to measure recovery time between back-to-back changes in PCIe. 
# Q261. Write FC code to check basic Polarity Inversion Detection during initialization in PCIe.
# Q262. Write FC code to cover false polarity detection in PCIe (reporting inversion when none exists).
# Q263. Write FC code to cover Successful Polarity Correction scenario in PCIe .(Polarity Correction Behavior)
# Q264. Write FC code to cover Polarity Changes During Recovery state in PCIe. (Polarity Inversion During Link Retraining)
# Q265. Write FC code to cover Cross-Lane Polarity Patterns scenario in PCIe. (Multi-Lane Polarity Combinations)
# Q266. Write FC code to cover lane reversal + polarity inversion combinations in PCIe.
# Q267. Write a covergroup to track the detection of lane reversal during PCIe link initialization. Include coverage points for both normal and reversed lane configurations.
# Q268. Implement a covergroup to verify that lane reversal is correctly handled across different link widths (x1, x4, x8, x16).
# Q269. How would you implement conditional coverage to verify lane reversal only when the link speed is greater than a certain threshold? Provide an example.
# Q270. Write a covergroup to track the transitions between normal and reversed lane configurations. How would you ensure all transitions are covered?
# Q271. Implement a covergroup to verify that lane reversal does not impact data integrity. Include coverage points for data checksums or CRCs.
# Q272. How would you parameterize a covergroup to handle different numbers of lanes in a PCIe design? Provide an example.
# Q273. How would you implement a covergroup to verify that lane reversal is correctly handled during hot-plug events?
# Q274. Write a covergroup to ensure that lane reversal is correctly handled across different PCIe generations (Gen1, Gen2, Gen3, Gen4,Gen5).
# Q275. Write a covergroup to verify lane reversal in designs with multiple PCIe lanes (e.g., x4, x8, x16)?
# Q276. Implement a covergroup to verify that lane reversal does not impact PCIe error reporting mechanisms. Include coverage points for error types.
# Q277. Write FC code to cover Invalid TLP Header Fields scenario in PCIe. (Malformed TLP Header Errors, May be due to invalid_fmt_type ,length_mismatch ,addr_alignment ,reserved_bits  violation etc)
# Q278. Write FC code to track ECRC validation failures on malformed TLPs in PCIe.
# Q279. Write FC code to cover Corrupted DLLP Detection in PCIe. (DLLP Framing Errors, May be crc_err,seq_err, or both)
# Q280. Write FC code to track stuffed symbol errors in DLLP framing .
# Q281. Write FC code to cover Invalid SKP OS Handling scenario with respect to differnet speed in PCIe.(SKP Ordered Set Corruption: like missing_skp,invalid_symbol/Bad symbol in SKP OS ,Incorrect SKP count etc)
# Q282. Write FC code to track clock tolerance compensation failures due to SKP errors.
# Q283. Write FC code to cover Electrical Idle Entry/Exit Error Scenario in PCIe.
# Q284. Write FC code to cover Data Link Layer CRC Error scenario in PCIe. (LCRC Validation Failures: Common bad CRC patterns like all_zeros ,all_ones ,common_flip)
# Q285. Write FC code to cover the ltssm state enters to Recovery state and triggering Framing Errors/ To track multiple recovery attempts for persistent framing errors (Framing Error Recovery).
# Q286. Write FC code to track error propagation when corruption occurs in the middle of a TLP data payload.
# Q287. Write FC code to cover Partial Packet Corruption scenario resulting Framing Errors (The Error location in packet may be at header or Payload or ECRC etc)
# Q288. Write FC code to cover 128b/130b encoding errors during Gen3→Gen4 transitions in PCIe.
# Q289. Write FC code to cover running disparity errors in 8b/10b encoding in PCIe.
# Q290. Write FC code to cover Basic LTSSM State Coverage in PCIe (Ensure that all possible state transitions are covered).
# Q291. Write FC code to track time spent in each of the LTSSM state in PCIe.
# Q292. Write FC code to cover all Valid LTSSM Transitions in PCIe.
# Q293. Write FC code to cover entry Reasons to Recovery State (May be due to skp_error,lane_failure/lane disabled ,dllp_crc error,EQ Failure etc)
# Q294. Write FC code to cover Configuration State Sub-States for achieving Link Width & Lane Number Negotiation in PCIe.
# Q295. Write FC code to track failed lane negotiations that fall back to fewer lanes in PCIe.
# Q296. Write FC code to track L0s/L1 Entry/Exit Sequences (Power State Transitions) in PCIe.
# Q297. Write FC code to cover Hot Reset Entry/Exit scenario in PCIe. (Hot Reset Behavior check)
# Q298. Write FC code to track TS1/TS2 sequence errors during Hot Reset , means the TS1/TS2 OS bits set for entering in to HOT Reset State in PCIe.
# Q299. Write FC code to cover Loopback Entry/Exit scenario in PCIe . (Loopback Behavior check)
# Q300. Write FC code to track TS1/TS2 sequence errors during Loopback , means the TS1/TS2 OS bits set for entering in to Loopback State in PCIe
# Q301. Write FC code to cover Disabled State Entry Scenario in PCIe.
# Q302. Write FC code to track TS1/TS2 sequence errors during Disabled State, means the TS1/TS2 OS bits set for entering in to Disabled State in PCIe.
# Q303. Write FC code track PERST# assertion during disabled state.
# Q304. Write FC code to cover EQ Phase Transitions in Recovery state in PCIe.
# Q305. How would you implement conditional coverage to verify LTSSM transitions only when the link width is x8 or greater? Provide an example.
# Q306. Write a covergroup to track the occurrence of LTSSM state transitions during link retraining. How would you ensure all retraining scenarios are covered?
# Q307. Implement a covergroup to verify that LTSSM transitions do not impact PCIe error reporting mechanisms. Include coverage points for error types.
# Q308. How would you implement a covergroup to verify that LTSSM transitions occur within specified timing constraints. For example : (DETECT -> POLLING and POLLING -> CONFIGURATION)
# Q309. Write FC code to implement a covergroup to verify LTSSM transitions in designs with dynamic lane reversal.
# Q310. How you would use functional coverage to identify potential deadlock scenarios within the LTSSM.
# Q311. Write FC code to implement a covergroup to verify LTSSM transitions during simultaneous link width and speed changes in PCIe
# Q312. Write FC code to implement a scenario like ,When a lane receives TS1s but the Link Control 2 register reports no lanes are enabled .(Ghost TS1 Detection in Polling)
# Q313. Write FC code to implement Odd/even lanes report opposite polarity during lane numbering in PCIe. (Config.Lanenum Accept with Mismatched Polarity)
# Q314. Write FC code to implement scenario like , Received FTS count doesn't match ordered set count in PCIe. (L0s Exit with Corrupted FTS)
# Q315. Write FC code to implement scenario like , Hot Reset occurs during Config.Linkwidth.Start in PCIe. (Hot Reset with Partial Configuration)
# Q316. Write FC code to implement scenario like , External loopback with lanes physically reversed in PCIe.(Loopback with Lane Reversal)
# Q317. Write FC code to implement scenario like ,Entering to Disabled state with non-empty transaction layer buffer .(Disabled State with Pending TLPs)
# Q318. Write FC code to cover scenario like , PHY skips Phase 2 EQ due to good margins in PCIe. (Equalization Phase Skipping)
# Q319. Write a covergroup to track the occurrence of hot reset events. Include coverage points for different link widths and speeds.
# Q320. How would you implement conditional coverage to verify hot reset behavior only when the link is operating at Gen3 or higher? 
# Q321. Write a covergroup to track the occurrence of hot reset events during simultaneous lane reversal. How would you ensure all scenarios are covered?
# Q322. Implement a covergroup to verify that hot reset does not impact PCIe error reporting mechanisms. Include coverage points for error types.
# Q323. Write FC code to implement a covergroup to verify hot reset behavior during PCIe link initialization.
# Q324. Write FC code to cover cases where Hot Reset is triggered during an active TLP transmission in PCIe.
# Q325. Write FC code to track TS1/TS2 Sequence Patterns During Hot Reset state in PCIe.
# Q326. Write FC code to cover scenario like , Hot Reset During Link Training in PCIe.
# Q327. Write FC code to cover Hot Reset with Pending Transactions in PCIe . (Outstanding TLPs During Reset)
# Q328. Write FC code to track unacknowledged DLLPs during Hot Reset in PCIe.
# Q329. Write FC code to cover Hot Reset During Low-Power State like L1, L0 etc
# Q330. Write FC code to cover Consecutive Hot Reset Operations in PCIe . {Hot Reset Stress Testing: Scenario be like , Gen1-> Gen3->Gen4->Gen5 (Link up done & achieved Max Supported speed, Then Speed Change to GEN2 , Then apply Hot Reset . Then again Speed Change to GEN2 , Then apply Hot Reset, Iterate it for 100 times )}
# Q331.
# Q332.
# Q333.
# Q334.
# Q335.
# Q336.
# Q337.
# Q338.
# Q339.
# Q340.
# Q341.
# Q342.
# Q343.
# Q344.
# Q345.
# Q346.
# Q347.
# Q348.
# Q349.
# Q350.

