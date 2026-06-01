# K Xuejie Case Review Skill

`KS-case-review` is a K Xuejie Skill for reviewing consulting case interview transcripts.

Paste a case interview transcript converted from audio, and the skill will identify the interviewer and candidate, diagnose the candidate's real performance, and generate a structured review report with concrete evidence and next-step practice suggestions.

> KS = K Xuejie Skill. This is the first skill in the K Xuejie consulting skill series.

## What It Does

This skill reviews one-on-one consulting case interview transcripts and produces:

- 6-dimension scoring
- Clarify, framework, communication, business thinking, calculation, and industry knowledge diagnosis
- Framework quality assessment
- Key case-solving blind spots
- A sharp one-sentence summary of the biggest issue
- Major problem list with transcript-based evidence
- Focused improvement direction and concrete practice actions
- Optional "business insight preview" for the case itself

## Input

Use a transcript converted from a case interview recording.

The transcript can be:

- pasted directly into chat
- provided as a local text file path
- labeled with speakers such as `Interviewer` / `Candidate`, `Q` / `A`, or raw speaker labels such as `SPEAKER_00`

The skill will infer which speaker is the interviewer and which speaker is the candidate.

## Output Structure

The main review report includes:

1. **6-Dimension Scoring**  
   Scores the candidate on clarify quality, framework communication, concise expression, viewpoint strength and case leadership, calculation process, and industry knowledge.

2. **Framework Quality Diagnosis**  
   Separates "how the framework was communicated" from "whether the framework itself was strong."

3. **Key Case-Solving Gaps**  
   Identifies the missing branches that materially affect the case conclusion.

4. **One-Sentence Summary**  
   A direct diagnosis of the candidate's biggest problem.

5. **Major Problem List**  
   Lists the most important issues with evidence from the transcript.

6. **Improvement Direction and Practice Plan**  
   Gives one priority improvement direction, concrete drills, and quick fixes for the next case.

## Business Insight Preview

After the performance review, the skill can optionally generate a business insight preview for the case itself.

This is a light version of a standard case answer. It uses the built-in framework library to explain:

- the key industry logic behind the case
- a standard framework mapped to the given case facts
- brainstorm directions the candidate missed
- better "hypothesis + judgment" phrasing
- 1-2 consultant-style takeaways
- a concise case conclusion

This helps the candidate understand not only "how I performed," but also "how this case should be thought about."

## Installation

Clone this repository into your local skills directory, or copy the repository folder into your Codex / agent skills folder.

Example:

```powershell
git clone https://github.com/love1272395498-beep/K-Xuejie-Case-Review.git "$env:USERPROFILE\.agents\skills\ks-case-review"
```

The skill folder should contain:

```text
ks-case-review/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── reference/
    ├── Case框架库-精简版.md
    └── 常见问题与练习库.md
```

## Usage

Invoke the skill with:

```text
KS-case-review
```

Example prompt:

```text
Use KS-case-review to review this case interview transcript:

<paste transcript here>
```

Chinese prompt examples:

```text
用 KS-case-review 帮我复盘这段 case 面试录音文稿。
```

```text
这段 case 录音转文字帮我看看，指出学员真实水平和下一步怎么练。
```

## About K 学姐

K 学姐是 Ex-MBB 咨询顾问，长期分享战略咨询面试、Case 训练和商业思维内容。这个 skill 基于 K 学姐日常做 Case 复盘的标准流程整理而成，目标是让每一次 mock 后的反馈更具体、更严格，也更能落到下一步练习。

全网同名「K 学姐」，可自行搜索。

