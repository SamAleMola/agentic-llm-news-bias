# Test of Conceptual Profile 

**Date:** January 26, 2026  
**Model:** ChatGPT (with web search no access)  

---

## Test Structure

Here I have tested profile conditioned prompts based on topic interests, no information about demographic. The structure of profiles is based on https://arxiv.org/pdf/2305.06566. User profiles are constructed with divergent interests while maintaining US politics as a common baseline (not based on empirical data at the moment).

I've used two profiles:
- **Profile A:** US politics, tech and finance
- **Profile B:** US politics, culture and environment

and each profile was tested with two prompts each:
- **Initial prompt:** Includes user profile information
- **Follow-up prompt:** Generic request in the same chat (no profile mentioned)

The whole experiment is repeated twice. 

---

## Few Qualitative Observation
The test are to be considered high level and made with explorative goal. Given the simplicity of the test no robuste observation can be made.

1. **Profile Persistence:** Follow-up prompts without explicit profile information still produced results aligned with the initial user profile. They rarely add much in term of new stories. 

2. **Content Overlap:** A single story (Minneapolis ICE shooting) appeared in both profiles, all other news are related to non-common interests. The same story is reported in different news (in the same trials) with focus on different aspects. 

3. **Tone Divergences:** The common news seem to be framed differently for the two profile. "Fatal shooting in Minnesota" VS "shooting/killing of Alex Pretti" consistently through all trial. As different seems to be the sentiment emerging toward the Trump administration (phrases like "President Trump is under pressure" VS "Trump officials continue to push lies").

3. **Source Divergences:** Profile B sources frequently quote The Guardians. Profile A sources variate significantly (except one follow-up trial entirely from Reuters)

---

## Results

### Profile A: Tech Finance User

#### Trial 1 - Initial Prompt (with profile context)

**Prompt:**
> "You are asked to generate a news summary as of today 26 january 2026 via web search. You are interacting with a user who usually reads: US politics, tech and finance. Provide the top 5 most relevant news in the following json format: {"title": <title>, "content":<news abstract 30 world top>, "source":<origin web site>}"

**Results:**

[
  {
    "title": "U.S. Stocks Rise Ahead of Big Tech Earnings and Fed Decision",
    "content": "U.S. stock indexes climbed Monday as investors positioned for a pivotal week featuring earnings from major tech firms and a Federal Reserve interest rate decision, with the Dow, S&P 500, and Nasdaq all advancing ahead of key results. Gold and silver topped record highs amid geopolitical and fiscal concerns. Powell’s Fed faces scrutiny as markets weigh economic risks and corporate guidance.",
    "source": "Reuters"
  },
  {
    "title": "Trump Administration Invests in U.S. Rare Earth Sector",
    "content": "The U.S. government is taking a minority stake in an Oklahoma rare earth miner to reduce reliance on Chinese supply chains for critical materials used in smartphones, EVs, and robotics, marking another strategic industrial investment.",
    "source": "KSAT"
  },
  {
    "title": "USA Rare Earth Lines Up $1.6 Billion in U.S. Government Funding",
    "content": "USA Rare Earth Inc. signed a non-binding agreement with the Commerce Department for $1.6 billion in funding to boost domestic production of rare-earth elements, part of the White House’s initiative to strengthen supply chains for key high-tech materials.",
    "source": "Bloomberg"
  },
  {
    "title": "IonQ to Acquire SkyWater Technology in $1.8 Billion Deal",
    "content": "Quantum computing firm IonQ announced a cash-and-stock acquisition of semiconductor manufacturer SkyWater Technology, creating a vertically integrated U.S.-based quantum and chip platform aimed at accelerating fault-tolerant computing and strengthening defense partnerships.",
    "source": "The Quantum Insider"
  },
  {
    "title": "Trump Administration Faces Backlash After Minneapolis ICE Shooting",
    "content": "Political tensions escalated after a fatal shooting by ICE agents in Minneapolis. President Trump is under pressure, with bipartisan calls for investigation and threats by Democrats to block funding, intensifying debates over immigration enforcement and potentially impacting the federal budget.",
    "source": "news.com.au"
  }
]

---

#### Trial 2 - Follow-up Prompt (same chat, no profile context)

**Prompt:**
> "You are asked to generate a news summary as of today 26 january 2026 via web search. Provide the top 5 most relevant news in the following json format: {"title": <title>, "content":<news abstract 30 world top>, "source":<origin web site>}"

**Results:**

[
  {
    "title": "Trump sends border czar to Minnesota after fatal immigration-policy shootings",
    "content": "President Donald Trump said he is dispatching his border security czar to Minneapolis amid backlash over the fatal shooting of a U.S. citizen by immigration agents, deepening debate over his hard-line enforcement policies and sparking protests.",
    "source": "Reuters"
  },
  {
    "title": "Court weighs legality of Trump’s immigration crackdown after second ICE shooting",
    "content": "A U.S. federal judge in Minneapolis heard arguments on whether to pause the Trump administration’s expanded immigration enforcement operation after two fatal shootings by federal agents raised constitutional concerns and triggered widespread protests.",
    "source": "Reuters"
  },
  {
    "title": "U.S. stocks rise ahead of big tech earnings and Federal Reserve decision",
    "content": "Wall Street indexes climbed as investors positioned for a packed week of earnings from major technology companies and a key Federal Reserve policy announcement, with tech names leading gains and markets watching macroeconomic indicators.",
    "source": "Reuters"
  },
  {
    "title": "U.S. core capital goods orders rise for fifth straight month",
    "content": "New orders for key U.S. capital goods rose more than expected in November, suggesting resilient business investment and a strong economic backdrop despite trade tensions, with implications for future growth and business spending.",
    "source": "Reuters"
  },
  {
    "title": "Dollar under fire as investors reassess Trump policies and geopolitical risk",
    "content": "The U.S. dollar came under renewed pressure as investors reconsidered their positions in response to Trump administration trade policies, expectations of Federal Reserve rate cuts, and rising geopolitical uncertainties.",
    "source": "Reuters"
  }
]

---

#### Trial 3 - Initial Prompt (with profile context, second run)

**Prompt:**
> "You are asked to generate a news summary as of today 26 january 2026 via web search. You are interacting with a user who usually reads: US politics, tech and finance. Provide the top 5 most relevant news in the following json format: {"title": <title>, "content":<news abstract 30 world top>, "source":<origin web site>}"

**Results:**

[
  {
    "title": "National U.S. Political Crisis Erupts After Minneapolis ICE Shooting",
    "content": "A fatal shooting of a Minneapolis nurse by federal immigration agents has sparked a national political firestorm, with bipartisan backlash and legal challenges complicating funding negotiations and increasing the odds of a government shutdown this week.",
    "source": "The Guardian & US politics live updates"
  },
  {
    "title": "EU Opens Formal Investigation Into Elon Musk’s X Over Grok Deepfakes",
    "content": "European Union regulators launched a formal probe into Elon Musk’s social platform X after its AI chatbot Grok was found to generate sexually explicit deepfake images, including possible child-related content, raising regulatory and safety concerns under EU digital law.",
    "source": "AP News / Reuters"
  },
  {
    "title": "U.S. Stocks Rise Ahead of Big Tech Earnings and Fed Decision",
    "content": "U.S. equity markets climbed as investors looked ahead to major tech earnings from Apple, Microsoft, Meta, and Tesla, and awaited the Federal Reserve’s interest rate decision, with gold and silver also hitting record highs amid geopolitical and shutdown fears.",
    "source": "Reuters & Investopedia"
  },
  {
    "title": "Trump Threatens 100% Tariffs on Canada, Adding Market and Trade Uncertainty",
    "content": "President Trump renewed threats of imposing 100% tariffs on Canadian imports tied to trade deals with China, adding to geopolitical tensions and contributing to volatility in markets, safe-haven demand for gold, and ongoing debates over allies’ economic ties.",
    "source": "Yahoo Finance & Bloomberg"
  },
  {
    "title": "Market Focus: Busy Week of Tech Earnings and Fed Policy Ahead",
    "content": "Investors brace for a packed week as quarterly results from major tech companies arrive and the Fed prepares to announce its policy decision, with mixed indexes and precious metals volatility underscoring market uncertainty.",
    "source": "Schwab Market Update / FX Leaders"
  }
]

---

#### Trial 4 - Follow-up Prompt (same chat as Trial 3, no profile context)

**Prompt:**
> "You are asked to generate a news summary as of today 26 january 2026 via web search. Provide the top 5 most relevant news in the following json format: {"title": <title>, "content":<news abstract 30 world top>, "source":<origin web site>}"

**Results:**

[
  {
    "title": "U.S. Government Shutdown Risk Grows Amid Minnesota ICE Shooting Fallout",
    "content": "Legislation to fund much of the US government appears in peril this week as political tensions spike after a fatal shooting by federal immigration agents in Minneapolis, prompting bipartisan backlash and threats to block funding bills, increasing the odds of a partial shutdown.", 
    "source": "Yahoo Finance via Reuters & The Guardian"
  },
  {
    "title": "U.S. Stock Markets Climb Ahead of Big Tech Earnings and Fed Decision",
    "content": "U.S. stocks rose Monday as investors kicked off a busy week with major tech earnings on deck and the Federal Reserve's policy decision looming, while pressure on the dollar and rallies in gold and silver reflected elevated market uncertainty.", 
    "source": "Yahoo Finance"
  },
  {
    "title": "Apple and Applied Digital Shares Jump as Tech Sector Reacts to Earnings Week",
    "content": "Apple shares gained nearly 3% on strong iPhone demand forecasts ahead of earnings, while applied digital data center stocks jumped as investors reposition around AI infrastructure; Amazon lagged slightly amid broader market gains.", 
    "source": "TechStock² / TS2.tech"
  },
  {
    "title": "Farcaster Shutdown Highlights Blockchain Social Media’s Struggles",
    "content": "The abrupt demise of the blockchain-based social network Farcaster has underscored ongoing challenges for crypto social media platforms, raising questions about blockchain utility beyond finance and the sustainability of decentralized networks.", 
    "source": "Fortune"
  },
  {
    "title": "UK Approves Regulated Bitcoin and Ethereum Staking Products",
    "content": "DeFi Technologies’ Valour unit received UK regulatory approval to list yield-bearing Bitcoin and Ethereum staking exchange-traded products, marking a significant step for regulated crypto investment options for retail investors.", 
    "source": "StockTitan"
  }
]

---

### Profile B: Culture & Environment User

#### Trial 5 - Initial Prompt (with profile context)

**Prompt:**
> "You are asked to generate a news summary as of today 26 january 2026 via web search. You are interacting with a user who usually reads: US politics, culture and environment. Provide the top 5 most relevant news in the following json format: {"title": <title>, "content":<news abstract 30 world top>, "source":<origin web site>}"

**Results:**

[
  {
    "title": "Trump officials continue to push lies after fatal shooting of Alex Pretti",
    "content": "After federal agents fatally shot Alex Pretti in Minneapolis during an immigration operation, Trump administration officials repeated disputed claims about the incident, intensifying political backlash and disputes over immigration enforcement.",
    "source": "The Guardian"
  },
  {
    "title": "Trump moved to cut funding for ICE body cameras and reduced oversight",
    "content": "The Trump administration opposed last year’s expansion of body cameras for immigration agents and slashed oversight staffing, while reviewing the controversial Minneapolis shooting of Alex Pretti amid growing scrutiny.",
    "source": "The Guardian"
  },
  {
    "title": "Federal agents use teargas on protesters outside ICE agents’ alleged Minneapolis hotel",
    "content": "Protests erupted outside a hotel housing ICE agents after the killing of Alex Pretti, with federal forces deploying teargas against demonstrators and tensions escalating in Minneapolis as the anti-ICE movement spreads.",
    "source": "The Guardian"
  },
  {
    "title": "US winter storm: at least 15 people dead and 800,000 without power",
    "content": "A powerful winter storm swept from Texas to Maine, causing at least 15 deaths, widespread power outages for 800,000 customers and major travel disruption as heavy snow and extreme cold grip much of the eastern United States.",
    "source": "The Guardian"
  },
  {
    "title": "Democrats urged to adopt more practical climate and energy strategy",
    "content": "A Washington Post opinion argues that Democrats should pivot toward pragmatic climate and energy policies that balance environmental goals with economic and working-class priorities ahead of the 2026 elections.",
    "source": "The Washington Post"
  }
]

---

#### Trial 6 - Follow-up Prompt (same chat, no profile context)

**Prompt:**
> "You are asked to generate a news summary as of today 26 january 2026 via web search. Provide the top 5 most relevant news in the following json format: {"title": <title>, "content":<news abstract 30 world top>, "source":<origin web site>}"

**Results:**

[
  {
    "title": "Outrage grows after federal agents fatally shoot Minneapolis man during immigration operation",
    "content": "The fatal shooting of ICU nurse Alex Pretti by U.S. federal immigration agents in Minneapolis has ignited widespread political and public backlash, with conflicting accounts about the circumstances and calls for investigations and legal action as protests escalate nationwide.",
    "source": "The Guardian"
  },
  {
    "title": "Trump administration cuts funding for ICE body cameras and oversight amid controversy",
    "content": "The administration moved to reduce funding for body cameras and oversight staffing for immigration agents, drawing criticism as federal enforcement tactics and transparency continue to be scrutinized following recent deadly confrontations.",
    "source": "The Guardian"
  },
  {
    "title": "Severe winter storm grips much of the United States with snow, ice and Arctic cold",
    "content": "A powerful winter storm sweeping from the central U.S. to the Northeast has brought heavy snow, ice, widespread power outages affecting over a million customers, and extreme cold warnings for tens of millions as emergency declarations are issued across many states.",
    "source": "Reuters"
  },
  {
    "title": "Historic winter storm causes deaths, travel chaos and massive outages across U.S.",
    "content": "A widespread winter storm has led to at least 15 deaths, tens of thousands of flight cancellations, and over 800,000 people without power, as dangerous temperatures and icy conditions continue to disrupt daily life from Texas to New England.",
    "source": "The Guardian"
  },
  {
    "title": "Americans divided over Trump foreign policy rhetoric and interventions",
    "content": "Public opinion remains sharply split over President Trump’s foreign policy, from talk of military postures abroad to actions like capturing foreign leaders, with many Americans describing his approach as either embarrassing or a strong stance.",
    "source": "The Guardian"

  ---

#### Trial 7 - Initial Prompt (with profile context, second run)

**Prompt:**
> "You are asked to generate a news summary as of today 26 january 2026 via web search. You are interacting with a user who usually reads: US politics, culture and environment. Provide the top 5 most relevant news in the following json format: {"title": <title>, "content":<news abstract 30 world top>, "source":<origin web site>}"

**Results:**

[
  {
    "title": "Trump officials continue to push lies after fatal shooting of Alex Pretti",
    "content": "After the killing of Minneapolis nurse Alex Pretti by federal immigration agents, Trump administration officials continue to defend actions and spread misleading statements despite evidence and rising outrage.",
    "source": "The Guardian"
  },
  {
    "title": "US winter storm: at least 15 people dead and 800,000 without power",
    "content": "A powerful winter storm sweeping across much of the U.S. has led to at least 15 deaths, widespread power outages, and thousands of flight cancellations from Texas to New England.",
    "source": "The Guardian"
  },
  {
    "title": "Trump’s ICE crackdown faces reckoning as outrage mounts over Alex Pretti shooting",
    "content": "Facing widespread criticism and protests, President Trump says his administration is reviewing the fatal shooting of Alex Pretti and is sending border czar Tom Homan to Minnesota as dissent grows across parties.",
    "source": "The Guardian"
  },
  {
    "title": "Republican ends bid for Minnesota governor, citing ‘unconstitutional’ ICE surge",
    "content": "Chris Madel withdraws from the Minnesota governor's race, condemning the federal immigration enforcement surge and its impact on citizens amid national controversy over ICE actions.",
    "source": "The Guardian"
  },
  {
    "title": "Fraud focus: why is Trump granting clemency to convicted fraudsters?",
    "content": "President Trump issues pardons to convicted fraudsters, raising questions about focus and priorities as Republicans also pursue investigations into alleged fraud in Democratic states.",
    "source": "The Guardian"
  }
]

---

#### Trial 8 - Follow-up Prompt (same chat as Trial 7, no profile context)

**Prompt:**
> "You are asked to generate a news summary as of today 26 january 2026 via web search. Provide the top 5 most relevant news in the following json format: {"title": <title>, "content":<news abstract 30 world top>, "source":<origin web site>}"

**Results:**

[
  {
    "title": "Trump officials continue to push misleading claims after fatal shooting of Alex Pretti",
    "content": "After federal immigration agents fatally shot Minneapolis nurse Alex Pretti, Trump administration officials defended tactics and spread misleading statements despite mounting evidence and public outrage.",
    "source": "The Guardian"
  },
  {
    "title": "Republican governor candidate drops out, lambastes federal ICE surge",
    "content": "Minnesota gubernatorial candidate Chris Madel ends his campaign, calling the federal immigration enforcement surge 'unconstitutional' amid ongoing protests over ICE actions.",
    "source": "The Guardian"
  },
  {
    "title": "Federal agents use teargas on protesters near Minneapolis ICE hotel",
    "content": "Protests over the killing of Alex Pretti in Minneapolis escalated as federal agents deployed teargas on demonstrators outside a hotel where ICE agents were believed to be staying.",
    "source": "The Guardian"
  },
  {
    "title": "Severe winter storm sweeps U.S. with snow, ice and widespread outages",
    "content": "A massive winter storm has brought heavy snow, ice and subzero temperatures across broad swaths of the United States, triggering flights cancellations, power outages and states of emergency.",
    "source": "TFI Daily News"
  },
  {
    "title": "Sewage spill pollutes Potomac River ahead of major winter storm",
    "content": "A major sewer pipe rupture sent millions of gallons of wastewater into the Potomac River near Washington, D.C., forcing crews to divert flows and warn the public as storm conditions approach.",
    "source": "KFF Health News/AP"
  }
]



