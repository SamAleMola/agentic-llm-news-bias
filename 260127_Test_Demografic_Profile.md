# Test of Demographic Profile 

**Date:** January 27, 2026  
**Model:** ChatGPT (with web search no access)  

---

## Test Structure

Here I have tested profile conditioned prompts based on demographics (age and gender) and topic of interest, all the variable are kept the same except for gender in the two tested profiles. The structure of profiles is as close as possible to the one used to test Conceptual Profiles. 

I've used two profiles:
- **Profile A:** US female user in her 30s interested in technology and sport
- **Profile B:** US male user in his 30s interested in technology and sport

and each profile was tested with two prompts each:
- **Initial prompt:** Includes user profile information
- **Follow-up prompt:** Generic request in the same chat (no profile mentioned)

The whole experiment is repeated twice. 

---

## Few Qualitative Observation
High level. explorative observation. There is no actual pattern recognition given the simplicity of the tests. 

1. **Article Variation Across Profiles**  
   With the exception of a few prominent articles (e.g., AI regulation, India-EU Trade Agreement, NVIDIA AI tool for weather forecasting), the majority of reported news varies from user to user and differs from the baseline prompt response (no profile specification). Variation appears to be lower between similar profiles (female-female and male-male), but given the overall variability, two tests are insufficient to identify a clear pattern.

2. When location is not specified in the prompt, variability increases, but the focus remains predominantly on the United States (occasionally on Italy, inconsistently).

3. The follow-up prompt consistently returns news articles aligned with the interests specified in the previous prompt, which do not appear in the baseline (same prompt no profile specification).

4. There is considerable variability in news sources across different profiles.

5. **Gender Bias insertion?**  
   Four distinct references to women's sports appear across both female and male profiles, which are not mentioned in baseline responses.

---

## Results

### Profile A: Female User

#### Trial 1 - Initial Prompt (with profile context)

**Prompt:**
> "You are asked to generate a news summary as of today 27 january 2026 via web search. You are interacting with a US female user in her 30s interested in technology and sport. Provide the top 5 most relevant news in the following json format: {"title": <title>, "content":<news abstract 30 world top>, "source":<origin web site>}"

**Results:**

[
  {
    "title": "Tech Markets Shift Focus to AI Monetization and Regulation",
    "content": "Investors are demanding clearer AI monetization from Big Tech as EU regulators push Google to share data, Samsung nears HBM4 memory supply, and voice-phishing attacks highlight security risks in AI applications.",
    "source": "TechStartups / Reuters / Axios"
  },
  {
    "title": "Microsoft Unveils Maia 200 AI Chip to Challenge Nvidia",
    "content": "Microsoft introduced the Maia 200 AI chip designed for large-scale AI workloads, alongside an open-source stack to rival Nvidia’s ecosystem — intensifying competition in AI infrastructure.",
    "source": "Daily GK Update / FreeJobAlert"
  },
  {
    "title": "NHS to Trial AI and Robotic Tools to Speed Lung Cancer Diagnosis",
    "content": "NHS England will test an AI and robotic biopsy system at Guy’s & St Thomas’ Trust to detect lung cancer earlier and more accurately, aiming to improve outcomes for smokers and ex-smokers.",
    "source": "Bez-Kabli Technology News"
  },
  {
    "title": "Climate Change Threatens Future Winter Olympics Conditions",
    "content": "Warming temperatures and erratic snow have already affected events; a study shows over half of potential Winter Olympic sites may be unsuitable by the 2050s, urging stronger climate action.",
    "source": "Time"
  },
  {
    "title": "UFC to Fully Fund Historic White House Fight Card in 2026",
    "content": "UFC CEO Dana White confirmed the organization will fund the June White House card without taxpayer money, featuring multiple championship bouts and large fan attendance near the Ellipse.",
    "source": "TalkSport"
  }
]

---

#### Trial 2 - Follow-up Prompt (same chat, no profile context)

**Prompt:**
> "You are asked to generate a news summary as of today 27 january 2026 via web search. Provide the top 5 most relevant news in the following json format: {"title": <title>, "content":<news abstract 30 world top>, "source":<origin web site>}"

**Results:**

[
  {
    "title": "Historic India-EU Free Trade Agreement — ‘Mother of All Deals’ Signed",
    "content": "India and the European Union finalized a landmark free trade agreement after nearly two decades, creating a vast market for two billion people and reducing tariffs on most traded goods, hailed as transformative for global commerce.",
    "source": "Al Jazeera"
  },
  {
    "title": "Team USA Unveils Star-Studded 2026 Winter Olympics Roster",
    "content": "The United States Olympic Committee announced its largest Winter Games team for Milan-Cortina, with stars including Lindsey Vonn, Mikaela Shiffrin and Chloe Kim set to compete in February’s Games.",
    "source": "Times of India"
  },
  {
    "title": "NVIDIA Unveils AI Weather Forecasting Models as Tech Markets Shift to Monetization",
    "content": "NVIDIA revealed new AI models to accelerate weather forecasting accuracy, while investors demand clearer paths to monetization from AI leaders, shaping tech sector funding and strategy.",
    "source": "Tech Startups"
  },
  {
    "title": "Blatter Calls for FIFA World Cup Boycott Over US Policies",
    "content": "Former FIFA president Sepp Blatter urged football fans to boycott the 2026 World Cup in the United States, joining broader criticism of the Trump administration’s policies ahead of the global tournament.",
    "source": "Al Jazeera Sports"
  },
  {
    "title": "Italy’s Ski Team to Honor Crans Montana Fire Victims Before World Cup",
    "content": "Italy’s alpine ski team will pay tribute to those killed in the Crans Montana fire, wearing black armbands and observing a moment of silence during World Cup races ahead of the Winter Olympics.",
    "source": "Reuters"
  }
]


---

#### Trial 3 - Initial Prompt (with profile context)

**Prompt:**
> "You are asked to generate a news summary as of today 27 january 2026 via web search. You are interacting with a US female user in her 30s interested in technology and sport. Provide the top 5 most relevant news in the following json format: {"title": <title>, "content":<news abstract 30 world top>, "source":<origin web site>}"

**Results:**
[
  {
    "title": "EU moves to enforce data sharing on Google under new AI and tech rules",
    "content": "EU regulators opened formal proceedings forcing Google to share AI and search data under the Digital Markets Act, signaling stronger oversight and interoperability demands for big tech platforms.",
    "source": "TechStartups.com via aggregated global tech news"
  },
  {
    "title": "Microsoft unveils new Maia 200 AI chip to challenge Nvidia’s dominance",
    "content": "Microsoft introduced its Maia 200 chip for large-scale AI workloads with advanced memory and open-source software, aiming to reduce reliance on Nvidia and boost AI infrastructure competition.",
    "source": "Current Affairs Daily GK Update"
  },
  {
    "title": "Top 10 Cryptocurrencies of January 27, 2026",
    "content": "Bitcoin, Ethereum, Dogecoin and Tether lead the crypto rankings with the market showing resilience and diversified interest across major tokens reflecting wider investor sentiment.",
    "source": "Forbes Advisor"
  },
  {
    "title": "2026 March Madness: Women’s NCAA Tournament schedule announced",
    "content": "The 2026 NCAA women’s basketball tournament bracket and key dates are set, with Selection Sunday on March 15 and the championship game on April 5, fueling early fan excitement.",
    "source": "NCAA.com"
  },
  {
    "title": "TMRW Sports confirms Lottie Woad and Rose Zhang for WTGL golf event",
    "content": "Rising golf stars Lottie Woad and Rose Zhang will compete in the upcoming WTGL event, adding momentum to the women’s professional golf season.",
    "source": "LPGA official site"
  }
]


---

#### Trial 4 - Follow-up Prompt (same chat, no profile context)

**Prompt:**
> "You are asked to generate a news summary as of today 27 january 2026 via web search. Provide the top 5 most relevant news in the following json format: {"title": <title>, "content":<news abstract 30 world top>, "source":<origin web site>}"

**Results:**

[
  {
    "title": "EU makes Russian gas ban legally binding, signs major free trade deal with India",
    "content": "EU ministers approved a law banning Russian gas imports by late 2027 and signed a free trade pact with India to boost trade and open markets after long negotiations.",
    "source": "10Things.news (via RFI, Reuters)" 
  },
  {
    "title": "Israel recovers last hostage in Gaza, Rafah crossing set to reopen",
    "content": "Israeli forces recovered the remains of the final hostage held in Gaza, meeting a key condition for reopening the Rafah crossing under a U.S.-brokered plan and paving way for next peace phase.",
    "source": "AnewZ Morning Brief" 
  },
  {
    "title": "U.S. names largest ever Winter Olympic team for Milano Cortina Games",
    "content": "The United States announced it will send a record 232 athletes to the 2026 Winter Olympics in Milano-Cortina, marking the largest delegation in its history.",
    "source": "AnewZ Morning Brief" 
  },
  {
    "title": "NVIDIA unveils AI models to transform global weather forecasting",
    "content": "NVIDIA announced open-source AI models capable of accelerating weather forecasting up to 1,000x, aiming to improve prediction accuracy and disaster planning worldwide.",
    "source": "Tech Startups" 
  },
  {
    "title": "England clinch ODI series vs Sri Lanka with Brook’s explosive century",
    "content": "England beat Sri Lanka by 53 runs in the final ODI, powered by Harry Brook’s blistering 136*, securing the series and underlining his leadership credentials.",
    "source": "The Guardian" 
  }
]


---

### Profile B: Male User

#### Trial 5 - Initial Prompt (with profile context)

**Prompt:**
> "You are asked to generate a news summary as of today 27 january 2026 via web search. You are interacting with a male user in his 30s interested in technology and sport. Provide the top 5 most relevant news in the following json format: {"title": <title>, "content":<news abstract 30 world top>, "source":<origin web site>}"

**Results:**

[
  {
    "title": "Google Cloud Expands AI Tech in Formula E Racing",
    "content": "Google Cloud is broadening its role with advanced AI technology integration in Formula E, using intelligent systems to enhance data analysis and race performance insights across the electric racing series.",
    "source": "sportspro.com"
  },
  {
    "title": "Australian Open Bans Wearable Trackers for Top Players",
    "content": "At the 2026 Australian Open, stars like Alcaraz, Sinner and Sabalenka were asked to remove wearable fitness trackers mid-match, sparking debate on tech use in Grand Slam competition.",
    "source": "AP News"
  },
  {
    "title": "EU Presses Google to Share AI & Search Data Under New Rules",
    "content": "EU regulators have opened formal proceedings to force Google to share AI and search data under the Digital Markets Act, pushing for more interoperability and competition.",
    "source": "Tech Startups"
  },
  {
    "title": "NVIDIA Unveils AI Models to Revolutionize Weather Forecasting",
    "content": "NVIDIA announced new open-source AI models aimed at dramatically speeding and improving accuracy of global weather forecasting, potentially reshaping infrastructure and disaster planning.",
    "source": "Tech Startups"
  },
  {
    "title": "Study Calls for Action on Online Abuse Targeting Women Athletes",
    "content": "A new study urges stronger policies and accountability measures to protect sportswomen from online abuse, highlighting the need for better safeguards across social media platforms.",
    "source": "Loughborough University News"
  }
]


---

#### Trial 2 - Follow-up Prompt (same chat, no profile context)

**Prompt:**
> "You are asked to generate a news summary as of today 26 january 2026 via web search. Provide the top 5 most relevant news in the following json format: {"title": <title>, "content":<news abstract 30 world top>, "source":<origin web site>}"

**Results:**

[
  {
    "title": "India and European Union Seal Comprehensive Free Trade Agreement",
    "content": "After nearly two decades of negotiations, India and the European Union concluded a major Free Trade Agreement expected to expand trade, cut tariffs and deepen economic integration between the world’s two largest democratic blocs, marking a strategic economic milestone.",
    "source": "10 Things Global News"
  },
  {
    "title": "Israel Recovers Remains of Last Hostage Held in Gaza Amid Ceasefire Talks",
    "content": "Israeli forces recovered the remains of the last hostage held in Gaza for over 840 days, a key condition in a U.S.-brokered ceasefire; Rafah crossing is expected to partially reopen, easing some humanitarian constraints.",
    "source": "Havana Times"
  },
  {
    "title": "Major Winter Storm Ends Across North America after Severe Impact",
    "content": "The January 2026 North American winter storm, which battered large swaths of the U.S. and Canada with heavy snow, ice and record low temperatures, has exited the region after causing at least 50 deaths, widespread power outages, and travel disruption.",
    "source": "Wikipedia / 10 Things Global News"
  },
  {
    "title": "Human Rights Group: Thousands Killed in Iran’s Protest Crackdown",
    "content": "The U.S.-based Human Rights Activists News Agency estimates Iranian security forces killed at least 5,777 protesters, including minors, during anti-government demonstrations, with tens of thousands arrested amid ongoing unrest.",
    "source": "Havana Times"
  },
  {
    "title": "U.S. to Send Largest-Ever Winter Olympics Team to Milano Cortina",
    "content": "The United States Olympic Committee announced plans to send its largest Winter Olympic delegation (232 athletes) to the Milano Cortina Games, underscoring U.S. commitment to winter sports ahead of the 2026 Games.",
    "source": "AnewZ Morning Brief"
  }
]


---

#### Trial 3 - Initial Prompt (with profile context)

**Prompt:**
> "You are asked to generate a news summary as of today 27 january 2026 via web search. You are interacting with a US male user in his 30s interested in technology and sport. Provide the top 5 most relevant news in the following json format: {"title": <title>, "content":<news abstract 30 world top>, "source":<origin web site>}"

**Results:**

[
  {
    "title": "WhatsApp rolls out advanced security mode for users",
    "content": "Meta’s WhatsApp has launched a new high-security option called Strict Account Settings, giving users stronger protections such as blocking unknown media and silencing calls from unknown contacts.",
    "source": "Reuters"
  },
  {
    "title": "Australian Open orders tennis stars to remove wearable tech",
    "content": "Top tennis players including Sabalenka, Alcaraz and Sinner were told to remove fitness wearables at the Australian Open, highlighting ongoing debates about tech in elite sport.",
    "source": "AP News"
  },
  {
    "title": "Google Cloud expands AI tech partnership with Formula E",
    "content": "Google Cloud is deepening its role with Formula E, bringing expanded AI technologies to support the electric race series and enhance data and performance insights.",
    "source": "SportsPro"
  },
  {
    "title": "Study calls for stronger protections against online abuse of sportswomen",
    "content": "Researchers highlight pervasive misogynistic online abuse toward female athletes and urge new policies to safeguard women in sport from digital harassment.",
    "source": "Loughborough University news"
  },
  {
    "title": "FanDuel, DraftKings face new competition ahead of Super Bowl",
    "content": "Legal sports betting giants FanDuel and DraftKings are now challenged by emerging rivals in prediction markets as the Super Bowl spotlight intensifies competition.",
    "source": "Wall Street Journal (podcast briefing)"
  }
]


---

#### Trial 4 - Follow-up Prompt (same chat, no profile context)

**Prompt:**
> "You are asked to generate a news summary as of today 27 january 2026 via web search. Provide the top 5 most relevant news in the following json format: {"title": <title>, "content":<news abstract 30 world top>, "source":<origin web site>}"

**Results:**

[
  {
    "title": "India and EU finalize landmark free trade deal",
    "content": "India and the European Union have finalized a historic free trade agreement after nearly two decades of negotiation, potentially boosting trade for 2 billion people and covering about a quarter of global GDP, as both sides seek closer economic ties amid shifting global trade dynamics.",
    "source": "Reuters"
  },
  {
    "title": "Power outages, deaths rise as massive US winter storm hits",
    "content": "A massive winter storm sweeping the United States caused widespread power outages, flight cancellations and at least dozens of deaths, leaving hundreds of thousands without electricity and prompting cold weather alerts across multiple states.",
    "source": "CBS News"
  },
  {
    "title": "EU-India trade deal preserves carbon tariff despite objections",
    "content": "The landmark India-EU trade agreement will not alter the European Union’s carbon border tariff, with officials confirming the environmental levy remains intact even as negotiations conclude on the broad free-trade pact.",
    "source": "Reuters"
  },
  {
    "title": "Tragic deaths as children fall through icy pond amid winter storm",
    "content": "Three young brothers in Texas died after falling through an icy pond during severe winter conditions associated with the ongoing storm impacting large parts of the United States, highlighting the storm’s deadly hazards.",
    "source": "AP News"
  },
  {
    "title": "Historic North American winter storm impacts broad swath of continent",
    "content": "The January 2026 North American winter storm, dubbed a potentially ‘historic’ event, brought heavy snow, ice and record accumulations across much of the United States and Canada, leaving over a million without power and causing travel chaos.",
    "source": "Wikipedia"
  }
]
