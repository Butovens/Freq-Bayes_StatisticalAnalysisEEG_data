# This is an example of frequentist and Bayesian statistical analysis of EEG data

The dataset **erp_data.csv** is from an EEG (electroencephalogram) experiment. Participants read sentences while electrical activity was recorded from their scalp. EEG activity time-locked to a specific critical stimulus (e.g., a word) is called an Event-Related Potential (ERP). In the electrophysiology literature, some time windows within ERPs have been associated with specific cognitive computations. For example, the “P600” a positive deflection of the ERP waveform, typically measured
between 600 and 800ms after the stimulus, is thought to index some kind of error detection process.

Some of the sentences in this experiment contained errors in the last word (e.g., typos like “He always told a
good anecdotes”) and some of them just have words that don’t make sense in the context of the sentence
(“He always told a good horse”). The Condition column contains information about what kind of error it is
(details not important for our purposes). Mean ERP amplitudes are in the MeanAmp column.

The sentences in this experiment were also given to an independent set of participants who were asked to
correct the last word of the sentence if they thought it contained an error. The results of that norming study
are in **erp_norms.csv**. The Intended Completion column counts how many times participants corrected
the word to the intended word (e.g., anecdote).

We want to know if the P600 amplitude is related to the probability that the intended word
can be recovered. To answer this question we first need to do some data wrangling before you can
jump into the analysis.