# Case Study: BottleDream Research Session

> A real-world demonstration of `social-org-research` in `depth: deep` mode.

## Background

**Target:** BottleDream (上海瓶凡人网络科技有限公司) — China's 5th B Corp™, first media-type B Corp, a social innovation content platform.

**Date:** September 2026

**Depth:** `deep` (4 iterations over 2 hours)

**Triggering user questions:**
1. "Help me deep-research BottleDream" (initial brief)
2. "Output as PDF attachment" (format requirement)
3. "Is the activity execution done by themselves, or by a contracted team?" (deep dive 1)
4. "Do volunteers / interns / co-creators get paid? What benefits?" (deep dive 2)
5. "Save this as a reusable prompt for similar research" (final ask — became this skill)

---

## Dimensions Executed (deep mode — all 10)

| # | Dimension | Sources consulted | Key finding |
|---|-----------|-------------------|-------------|
| 1 | Company body | 爱企查, 天眼查, B Lab | 2 legal entities: 广州市开个瓶子网络科技有限责任公司 + 上海瓶凡人网络科技有限公司 (2017-01-12, ¥1M reg, ¥90K paid-in, ¥500K realized). Founder 蔡延青 as legal rep. |
| 2 | Brand & history | 36氪, 凤凰网, LinkedIn, WEF | Founded 2011-06-01; co-venture cofounder 衷声 CEO since 2016; B Corp certified 2017-08-03 (中国内地第五家, 首家媒体型) |
| 3 | Business model | 36氪 2017, Impact Garden | Two revenue axes: media business + Bottleverse sponsorship; breakeven by 2017; NO equity funding disclosed |
| 4 | Content & methodology | 36氪 衷声 1-on-1, China Development Brief, 一席 | "Appreciative Inquiry" + #For Good# framework; daily-life categorization instead of academic; ~1000 changemaker stories, 200M cumulative reach |
| 5 | Activity system | 36氪 long-form retrospective, Sina Finance 2019, NetEase 2025 | Bottleverse festival (2016-2025, 5 editions); 10 core team + 100 volunteers for 2017 second edition; 65 co-creators; 520 attendees + 11M livestream + 180M exposure |
| 6 | People incentives | WonderCV 2026 intern posting, NetEase 2025 volunteer recruitment | 5 identity types with different incentive models; **interns: subsidized (¥150-200/day est.); volunteers: NO cash, only meal + T-shirt + immersive experience (housing/travel self-funded except 6 "guest angels")** |
| 7 | Co-creation network | Sina Finance 2019, NetEase 2025, Impact Garden | 5 categories: joint hosts (FAO/WWF/SK/小红村) + strategic (Unilever/JD/Robam/IKEA/SK) + content (200+ changemakers) + venue (西岸艺术中心/安吉余村) + platform (Weibo/Youku/NetEase) |
| 8 | Team & culture | LinkedIn, WonderCV, WEF | 5 core team members, mostly media/journalism backgrounds; "gentle CEO" culture; visible volunteer culture (BD staff volunteer at other NGOs) |
| 9 | Funding & legal | Narada Foundation, LinkedIn, 爱企查 | ¥4万 from Narada Foundation 2016 (small grant); ¥0 disclosed equity funding; MIT stands at ¥100K registered / ¥9K paid-in (likely under-stated) |
| 10 | Information gaps | Cross-referenced | Annual revenue/profit, employee headcount, intern salary exact, volunteer count per edition, partner ROI — all "not publicly disclosed" |

---

## Output Artifacts

| Artifact | Size | Verification |
|----------|------|---------------|
| `bottledream-research.md` (Markdown source) | 40.6 KB | Single source of truth for the report |
| `bottledream-research.pdf` (PDF deliverable) | 2.35 MB, 18 pages A4 | VBC: 35 source links = 35 matched links = 42 /Link rectangles; all URIs HTTP(S); Chinese rendering OK |

---

## Three Iterative Deep-Dives

The user's research questions evolved from a single "tell me about BottleDream" into three follow-up probes — exactly the kind of iterative behavior this skill supports.

### Deep dive 1: Activity execution model

**User question:** "Is the event execution done by themselves, or by a contracted team?"

**Skill execution:**
- Pulled 36氪 long-form retrospective from CEO 衷声 (the canonical "how we built Bottleverse 2017" article)
- Cross-referenced with Sina Finance 2019 third edition recap
- Pulled WonderCV 2026 intern posting for role definitions
- Pulled Journal of Futures Studies 2021 academic paper citing BD as example

**Output:** Added 9-section "Activity execution model" sub-chapter with role split table (BD core team / volunteers / co-creators / 3rd-party vendors), per-edition staffing data, 4 worked co-creation examples (禾然有机 / 老板电器 / SK集团 / 小红书公益).

### Deep dive 2: People incentives

**User question:** "Do volunteers / interns / co-creators get paid? What benefits? How do they attract volunteers?"

**Skill execution:**
- Pulled NetEase 2025-05-16 volunteer recruitment post (the canonical "what we offer volunteers" doc)
- Pulled WonderCV 2026 intern posting (the canonical "what we offer interns" doc)
- Cross-referenced with industry salary benchmarks (益盒 Charity Box: ¥133-177/day, 恩派: ¥100-120/day)
- Pulled *Volunteer Service Regulations* (志愿服务条例) for legal framework

**Output:** Added 8-section "People incentives" sub-chapter with 5-identity table, full volunteer benefits list (5 non-cash hooks), intern compensation structure (3 salary estimates), co-creator value exchange model, financial flow diagram (who pays whom), industry comparison table.

### Outcome: Skill meta-reflection

**User question:** "Save this as a reusable prompt for similar research."

**Skill execution:** The skill's own existence. The 10 dimensions and 8 Pitfalls were distilled directly from this session's evidence.

---

## Lessons Learned (encoded into the skill)

| Lesson | Source |
|--------|--------|
| "Registered capital ≠ actual scale" — always cross-check LinkedIn + B Lab + office size | BottleDream's ¥9K paid-in vs. 11-50 employees on LinkedIn |
| "Co-creator ≠ sponsor" — clarify before designing the survey | BD's partner relationships are all co-creation, not sponsorship |
| "Volunteers in China are statutorily unpaid" — separate the legal fact from the benefits discussion | Volunteer Service Regulations |
| "5 non-cash hooks" framework for explaining how non-monetary organizations attract people | Derived from BD's volunteer value proposition |
| "MD is single source of truth" + "VBC the links PDF" | Output deliverable structure |
| "Founder story ≠ org reality" — separate 阿菜's personal narrative from the team's day-to-day execution | 阿菜's social work degree + 腾讯 background vs. day-to-day execution by 衷声 / 邹嫣然 / 范文昊 |

---

## Reproducing This Case

To run an equivalent research session:

```
Research BottleDream, depth: deep
```

Or, more generally, replace "BottleDream" with any other social innovation organization. The skill will run all 10 dimensions and produce equivalent Markdown + PDF outputs.
