# gamification_research_analysis
This research was held in a University in South Korea where students and professors were interviewed in focus groups to address application of gamification in higher education.
<img width="49%" alt="image" src="https://github.com/user-attachments/assets/2bc7efa6-c1c3-4da0-9c41-3a35077f4ac5" /> <img width="49%" alt="image" src="https://github.com/user-attachments/assets/dc66be8e-1cb5-4f74-8249-e35b11595050" />


### Data Preprocessing & Cleaning Pipeline
Before applying any analytical models, a strict text-cleaning pipeline was executed to convert raw focus group audio transcripts into structured data and eliminate conversational noise:
* **Filler Word Filtering:** Stripped out spoken conversational crutches and fillers unique to verbal interviews (e.g., *'okay'*, *'just'*, *'like'*, *'right'*).
* **Stopword Removal:** Eliminated standard grammatical filler terms (e.g., *'the'*, *'is'*, *'and'*, *'a'*) using standard NLP stopword lists so only high-intent, substantive words remained.
* **Text Normalization:** Standardized all text to lowercase and removed punctuation to ensure terms (like *"Gamification"* and *"gamification"*) were counted and mapped accurately together.

## Analytical Methods
The four methods were selected specifically because they are appropriate for spoken focus group data, which differs from written text. Spoken language is repetitive, colloquial, and emotionally dense — methods suited to formal writing (such as TF-IDF or document-level topic modelling) would not produce reliable results. The selected methods work bottom-up from the actual words spoken.

### 1.	Word Frequency Analysis
Word frequency analysis counts how often meaningful terms appear across the entire transcript after filtering out grammatical filler words (stopwords) such as 'the', 'okay', 'just', and 'like'. What remains are the substantive words that each group chose to use repeatedly.

#### Why it was used:
Frequency is the most direct measure of where a speaker's attention naturally rests. It does not impose the researcher's interpretation — it simply reveals which concepts dominated each group's speech. When professors say 'reward' 47 times and 'frustrating' only twice, while students say 'frustrating' 18 times, that asymmetry is itself a research finding.

#### Limitation: 
Word frequency does not capture context or meaning. The word 'reward' could appear in a positive or negative sentence. This is why it is used in combination with the other methods below.

<img width="969" height="363" alt="image" src="https://github.com/user-attachments/assets/90335781-a347-41f2-960d-a94cce207660" />

## Data Analysis Results and Interpretation
The bar charts below show the top ten most frequently used substantive terms by each group after stopword removal. Each bar represents the raw count of how many times that word appeared across the full transcript.
 
#### What the data shows
The professor list is led by 'reward' (47), 'understand' (31), 'work' (27), and 'real' (24). These terms point to a consistent concern with whether gamification produces genuine learning outcomes and whether it transfers to real-world contexts. 'Implement' (19) and 'tools' (15) confirm that professors speak from the position of architects and evaluators of the system.

The student list is led by 'marks' (23), 'engaging' (20), 'frustrating' and 'quiz' (18 each), and 'rewards' (17). The near-equal frequency of 'engaging' and 'frustrating' is among the most important observations in the entire dataset. Students are not uniformly positive or negative — they hold a genuinely ambivalent relationship with gamification, experiencing both its appeal and its costs almost simultaneously.

#### Key divergence: 
The word 'frustrating/frustration' appears a combined 34 times in student speech and fewer than 5 times in professor speech. This gap foreshadows the sentiment findings in Section 4.3.


### 2.	Thematic Coding
Thematic coding organises individual words into pre-defined conceptual categories (themes) based on semantic similarity. For example, the words 'reward', 'points', 'badges', 'marks', and 'certificate' all express the same underlying concept — external reinforcement — and are grouped into the theme Motivation & Rewards.

#### Why it was used: 
This method directly bridges raw transcript data to the theoretical framework of the study. Eight themes were defined, each mapped to one of the three analytical lenses: Behaviorist Learning Theory (Skinner), Flow Theory (Csikszentmihalyi), and Self-Determination Theory (Deci & Ryan). By counting how often each group falls into each theme, the data can be compared against theoretical predictions.

#### Justification for this study: 
Focus group research produces qualitative data that is typically analysed by close reading. Thematic coding adds a quantitative layer that makes it possible to compare two groups systematically and state, for example, that students referenced frustration-related concepts 133% more than professors did — not as an impression, but as a measured count.

<img width="969" height="364" alt="image" src="https://github.com/user-attachments/assets/d70b0814-c564-4158-8071-2297d1d0e55b" />

The grouped bar chart above shows how frequently each group's language fell into each of the eight pre-defined analytical themes. Each theme is mapped to one of the three theoretical frameworks underpinning this study.
  
#### Motivation & Rewards (Behaviorism):
Both groups score comparably here (69 vs 85), confirming that reward-system thinking is central to how both professors and students conceptualise gamification. Skinner's reinforcement model is implicitly present in the discourse of both groups.

#### Learning Outcomes (Behaviorism/SDT): 
Professors score notably higher (121 vs 88). This is the theme professors discuss most overall — they are fundamentally concerned with whether gamification produces measurable learning. Students discuss outcomes too, but their discourse is spread more evenly across experiential themes.

#### Frustration & Barriers: 
Students score more than double (98 vs 42). This is the single largest divergence in the dataset. Cheating, time pressure, unfair quiz design, and loss of marks are raised repeatedly by students but receive far less attention from professors. This is the clearest evidence of the perceptual gap between the two groups.

#### Engagement & Flow (Flow Theory): 
Students score 2.5 times higher (48 vs 19). Students feel and describe the quality of their own engagement much more explicitly than professors. When professors discuss engagement it tends to be abstract ('students seemed more engaged'); when students discuss it they describe the felt experience of being drawn in or shut out.

#### Technology & Tools: 
The largest absolute gap in the dataset — professors score 92 vs students' 38. This confirms that professors frame gamification primarily as a technology design challenge, while students rarely initiate discussions about the tools themselves.

#### Competition & Leaderboards: 
Students score nearly five times higher (44 vs 9). Competition dynamics are intensely present in student experience but barely register in professor discourse — suggesting professors do not fully appreciate the social and psychological pressure their competitive structures create.

#### Autonomy & SDT: 
Students score 2.5 times higher (35 vs 14). Self-direction, choice, and self-paced learning are significantly more prominent in student speech. Students repeatedly contrast compulsory subjects — where gamification feels coercive — with voluntary, self-chosen tools where it is experienced positively.


### 3.	Sentiment Analysis
Sentiment analysis classifies language as carrying positive or negative emotional signals. A list of positive words ('good', 'effective', 'engaging', 'enjoy', 'benefit') and negative words ('difficult', 'stress', 'fail', 'cheat', 'unfair') was compiled and counted across each transcript. The ratio of positive to negative signals then characterises each group's overall emotional orientation toward gamification.

#### Why it was used: 
Attitude toward gamification is central to this research. Sentiment analysis quantifies what might otherwise be described only in vague terms ('professors seemed more positive than students'). A ratio of 2.16 (professors) vs 0.91 (students) is a precise, citable finding that can be discussed in terms of structural differences — professors design gamification from a position of authority, while students receive it under conditions of assessment pressure.

#### Limitation: 
Lexicon-based sentiment analysis can miss sarcasm and context. A phrase like 'the reward was pointless' would count 'reward' as positive when the meaning is negative. This limitation is acknowledged and is why findings are interpreted alongside the qualitative thematic analysis.

<img width="969" height="364" alt="image" src="https://github.com/user-attachments/assets/e23be934-2146-41ac-924a-1f1960968b9c" />

The charts below compare the volume of positive and negative language signals across both groups, and express the relationship as a ratio.
 
#### Interpretation
Professors used 123 positive signals and 57 negative signals — a ratio of 2.16. They are broadly, though not unconditionally, positive about gamification. Their negative language tends to cluster around concerns about implementation difficulty, academic integrity, and the limits of gamification in precision-sensitive fields.

Students used 121 positive signals and 133 negative signals — a ratio of 0.91. This near-parity is a crucial finding. Students are not anti-gamification; they experience its appeal directly. But for every positive aspect they identify, they identify an equally weighted negative — unfair systems, stress, cheating by others, and a feeling that games distract from real learning.

#### Research significance: 
The 2.16 vs 0.91 sentiment gap cannot be explained by preference alone. It reflects a structural difference: professors design gamification from a position of control and authority; students receive it under conditions of assessment pressure, competitive comparison, and limited autonomy. This asymmetry should inform how gamification is implemented and evaluated in higher education.




### 4.	Co-occurrence Analysis
Co-occurrence analysis identifies which key concepts appear together within the same sentence. When two terms co-occur in a speaker's sentence, it signals that they are mentally linked — the speaker connects those two ideas in real time. For example, if a student says 'the leaderboard makes me stressed', they have linked 'leaderboard' and 'stress' in a single thought.

#### Why it was used:
Co-occurrence reveals the cognitive associations that participants hold — something that word frequency and thematic coding cannot capture. A single word appearing 20 times tells us it matters; two words appearing together 3 times tells us how it matters in relation to something else. For qualitative research, these paired concepts become the richest material for interpretation.

#### Most significant finding: 
The pair 'practical + theory' co-occurs repeatedly in student speech — suggesting students consistently feel a gap between the surface activity of gamification and genuine conceptual understanding. This was not asked about directly; it emerged organically from the data.

<img width="906" height="414" alt="image" src="https://github.com/user-attachments/assets/2cf2b3e9-7b87-4bcb-9666-f5e17c541fe3" />

The chart below shows which pairs of key concepts appeared together within the same sentence across both transcripts. Only student data produced meaningful co-occurrence patterns; professor speech was more fragmented across topics.
 
#### Interpretation
The most frequent student pair is 'badges + points' (3 co-occurrences), indicating that students mentally bundle gamification mechanics together. They do not think of badges and points as separate design choices — they experience them as a unified reward system.

The pair 'practical + theory' (2 co-occurrences) is among the most analytically significant. Students repeatedly raise this pairing in the context of frustration — they feel that gamification, as they have experienced it, stays at the level of surface activity without building genuine conceptual understanding. This finding directly supports the critical dimension of the research: that gamification can produce visible engagement without producing deep learning.

The pair 'leaderboard + stress' confirms what the thematic coding and sentiment data suggest independently: for students, competition is emotionally costly. The two concepts are mentally linked, not separate. When students think of leaderboards, stress is part of the same thought.

Professor co-occurrences are sparse (only 2 pairs, each appearing once). This is not because professors lack views — the word frequency data shows they speak extensively. Rather, they tend to discuss concepts in isolation rather than in combination. This further supports the interpretation that professors think analytically about individual design elements, while students experience them holistically.


### Word Frequency Visualizations
The word clouds below provide an immediate visual impression of each group's dominant vocabulary. Word size is proportional to frequency — larger words appeared more often. Filler words, greetings, and common grammatical words have been filtered out, leaving only substantive content terms.

#### Interpretation guide: 
The most prominent words in each cloud represent the concepts that group most naturally gravitates toward when discussing gamification. Comparing the two clouds side by side reveals how different each group's frame of reference is.

#### Professors — Word Cloud
 
The professor word cloud is dominated by terms such as reward, tools, understand, technology, engineering, simulation, cognitive, and algorithm. This vocabulary reveals that professors approach gamification from a pedagogical design perspective — they think in terms of what tools to implement, what system to build, and what outcomes to measure. Notably, words such as 'general', 'depend', and 'works' suggest a conditional, context-sensitive stance: professors do not universally endorse gamification but discuss when and how it applies.

<img width="969" height="484" alt="image" src="https://github.com/user-attachments/assets/1a5639c3-3095-4f0c-a0ba-4f3ca8108476" />


#### Students — Word Cloud
 
The student word cloud is strikingly different in character. Dominant terms include frustration, engaging, marks, leaderboard, experience, practical, points, badges, and frustrating. Students speak the language of lived experience — what they felt, what motivated them, and where the system failed them. The simultaneous prominence of 'engaging' and 'frustrating/frustration' is particularly telling: students hold genuinely mixed feelings, with gamification generating both enthusiasm and significant irritation in roughly equal measure.

<img width="969" height="484" alt="image" src="https://github.com/user-attachments/assets/85f5fe6c-4071-4832-991b-980ab50a0c0e" />


 
