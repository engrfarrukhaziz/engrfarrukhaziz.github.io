---
layout: compress
permalink: /publications/
---

{% include base_path %}

<!doctype html>
<html lang="{{ site.locale | slice: 0,2 }}" class="no-js"{% if site.site_theme == "dark" %} data-theme="dark"{% endif %}>
  <head>
    {% include head.html %}
    {% include head/custom.html %}
    <style>
      body {
        font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
        background-color: #f4f7fa;
        color: #222;
        margin: 0;
        padding: 0;
      }
      .masthead {
        background-color: #012a4a;
        color: #fff;
        text-align: center;
        padding: 1.8rem 1rem;
        font-weight: 700;
        font-size: 1.6rem;
        letter-spacing: 1.3px;
      }
      main {
        width: 100%;
        max-width: 1500px;
        margin: 3rem auto 5rem;
        background: white;
        border-radius: 12px;
        box-shadow: 0 10px 30px rgb(0 0 0 / 0.1);
        padding: 2.5rem 2rem;
        text-align: center;
        position: relative;
      }
      .profile-pic {
        width: 140px;
        height: 140px;
        border-radius: 50%;
        object-fit: cover;
        margin: 0 auto 1.8rem;
        border: 3px solid #007acc;
        box-shadow: 0 4px 10px rgba(0, 122, 204, 0.4);
      }
      h1 {
        font-size: 2.4rem;
        color: #012a4a;
        margin-bottom: 0.2rem;
      }
      h2 {
        font-weight: 400;
        color: #005f99;
        margin: 0 0 1.8rem 0;
        font-size: 1.2rem;
        letter-spacing: 0.6px;
      }
      p.intro {
        font-size: 1.1rem;
        line-height: 1.55;
        color: #333;
        margin-bottom: 2.8rem;
        padding: 0 1rem;
      }
      .btn-primary {
        background-color: #007acc;
        color: white;
        font-weight: 600;
        font-size: 1.15rem;
        padding: 0.85em 2.4em;
        border-radius: 8px;
        text-decoration: none;
        box-shadow: 0 4px 14px rgb(0 122 204 / 0.4);
        transition: background-color 0.3s ease, box-shadow 0.3s ease;
        cursor: pointer;
        user-select: none;
        display: inline-block;
      }
      .btn-primary:hover,
      .btn-primary:focus {
        background-color: #005f99;
        box-shadow: 0 6px 20px rgb(0 95 153 / 0.6);
        outline: none;
      }
      .dropdown-links {
        margin-top: 1rem;
        text-align: left;
        max-width: 320px;
        margin-left: auto;
        margin-right: auto;
        background: #e7f0fa;
        border-radius: 8px;
        box-shadow: 0 4px 12px rgb(0 122 204 / 0.2);
        display: none;
        padding: 1rem 1.5rem;
        font-size: 1rem;
      }
      .dropdown-links a {
        display: block;
        color: #007acc;
        font-weight: 600;
        text-decoration: none;
        margin-bottom: 0.6rem;
        border-bottom: 1px solid transparent;
        padding-bottom: 4px;
        transition: border-color 0.25s ease;
      }
      .dropdown-links a:last-child {
        margin-bottom: 0;
      }
      .dropdown-links a:hover,
      .dropdown-links a:focus {
        border-bottom: 1px solid #007acc;
        outline: none;
      }
      footer {
        text-align: center;
        font-size: 0.9rem;
        color: #555;
        padding: 2rem 1rem 1rem;
        letter-spacing: 1.2px;
        border-top: 1px solid #ddd;
        background: #fff;
      }
      footer a {
        color: #007acc;
        text-decoration: none;
        font-weight: 600;
        margin: 0 0.5rem;
      }
      footer a:hover,
      footer a:focus {
        text-decoration: underline;
        outline: none;
      }
      footer .contact-email {
        display: block;
        margin-bottom: 0.5rem;
        font-weight: 700;
        color: #222;
      }
      /* New styles for supervisors and collaborators */
      .section-heading {
        background-color: #007acc;
        color: white;
        font-weight: 700;
        font-size: 1.5rem;
        padding: 0.6rem 1rem;
        border-radius: 8px;
        margin: 3rem 0 1.5rem;
        text-align: left;
        max-width: 1500px;
        width: 100%;
        margin-left: auto;
        margin-right: auto;
      }

      .person-info {
        max-width: 1500px;
        width: 100%;
        margin-left: auto;
        margin-right: auto;
        text-align: left;
        font-size: 1rem;
        line-height: 1.4;
        color: #222;
        padding: 0 1rem;
      }

      .person-info a {
        color: #007acc;
        text-decoration: none;
        font-weight: 600;
        margin-right: 1rem;
      }

      .person-info a:hover,
      .person-info a:focus {
        text-decoration: underline;
        outline: none;
      }

      .person-name {
        font-weight: 700;
        margin-top: 0.6rem;
      }

      /* Publications styles */
      #publications {
        max-width: 1500px;
        width: 100%;
        margin: 2rem auto;
        padding: 0 1rem;
        text-align: left;
      }
      #publications h1 {
        border: 3px solid #007acc;
        color: #012a4a;
        padding: 0.5rem 1rem;
        font-weight: 700;
        font-size: 2rem;
        display: inline-block;
        margin-bottom: 1.5rem;
        border-radius: 8px;
      }
      #publications article {
        border-bottom: 1px solid #ddd;
        padding-bottom: 1.4rem;
        margin-bottom: 1.4rem;
      }
      #publications article:last-child {
        border-bottom: none;
      }
      #publications h2 {
        font-size: 1.25rem;
        margin-bottom: 0.25rem;
        color: #005f99;
      }
      #publications .authors-journal {
        font-style: italic;
        font-size: 0.95rem;
        margin-bottom: 0.7rem;
        color: #555;
        line-height: 1.3;
      }
      #publications .btn-link {
        display: inline-block;
        padding: 0.5em 1.2em;
        margin-top: 0.2rem;
        margin-right: 0.6rem;
        background-color: #007acc;
        color: white;
        font-weight: 600;
        border-radius: 6px;
        text-decoration: none;
        box-shadow: 0 3px 8px rgb(0 122 204 / 0.4);
        transition: background-color 0.3s ease, box-shadow 0.3s ease;
      }
      #publications .btn-link:hover,
      #publications .btn-link:focus {
        background-color: #005f99;
        box-shadow: 0 5px 15px rgb(0 95 153 / 0.6);
        outline: none;
      }

      @media (max-width: 480px) {
        h1 {
          font-size: 2rem;
        }
        .profile-pic {
          width: 120px;
          height: 120px;
        }
        .dropdown-links {
          max-width: 100%;
          padding: 1rem;
        }
        .section-heading {
          max-width: 100%;
          font-size: 1.3rem;
        }
        .person-info {
          max-width: 100%;
          padding: 0 0.5rem;
          font-size: 0.95rem;
        }
        #publications {
          padding: 0 0.5rem;
        }
      }
    </style>
  </head>

  <body>

    {% include browser-upgrade.html %}

    <header class="masthead">
      Dr. Farrukh Aziz
    </header>

    <main>
      <img src="https://avatars.githubusercontent.com/u/225464808?s=400&u=ae925ec37e6c6d11e9ad1cd4f2fc32cf90d4c041&v=4" alt="Dr. Farrukh Aziz" class="profile-pic" />

      <h1>Dr. Farrukh Aziz</h1>
      <h2>PhD Researcher | AI, Behavioral Science & Eng.Management Specialist</h2>

      <p class="intro">
        Welcome! I am a dedicated researcher at Dalian University of Technology, China, focusing on pioneering interdisciplinary studies where artificial intelligence meets organizational behavior and strategic management.<br /><br />
        My mission is to leverage cutting-edge AI to unlock new insights in leadership effectiveness, lean manufacturing, and financial risk, enabling smarter decision-making and sustainable growth for industries worldwide.
      </p>

      <button class="btn-primary" id="researchToggleBtn" aria-expanded="false" aria-controls="researchLinks">
        Explore My Research & Publications
      </button>

      <nav class="dropdown-links" id="researchLinks" aria-label="Research and profile links" role="region">
        <a href="/research-projects" target="_blank" rel="noopener noreferrer">Research Projects</a>
        <a href="/publications" rel="noopener noreferrer">Research Publications</a>
        <a href="https://scholar.google.com/citations?hl=en&user=ulUkkPus9M0C" target="_blank" rel="noopener noreferrer">Google Scholar</a>
        <a href="https://www.researchgate.net/profile/Farrukh-Aziz-6" target="_blank" rel="noopener noreferrer">ResearchGate</a>
        <a href="https://orcid.org/0000-0001-7088-0371" target="_blank" rel="noopener noreferrer">ORCID Profile</a>
      </nav>

      <section id="publications" aria-label="Research Publications">
        <h1>Research Publications</h1>

        <article>
          <h2>How job stressors affect project-oriented OCB: An ego depletion perspective</h2>
          <div class="authors-journal">
            F Aziz, FA Shah, HM Shah<br />
            International Research Journal of Modernization in Engineering Technology, 2020
          </div>
          <a href="https://www.researchgate.net/publication/394407153_HOW_JOB_STRESSORS_AFFECT_PROJECT_ORIENTED_OCB_AN_EGO_DEPLETION_PERSPECTIVE?_sg%5B0%5D=-h2qnk7J5HT7c4fmpz1JkH3ooPzQooL35pGMsKAYR4PXTL3mG26rtCBB7Frl0Zx8AZPOK2FNpqaJrO13OuS6MBWRqd3M9vto4yZuJpyP.I2z0pRIPIMRwuED6FkMd6eVda9XHUpScitFmCBDzQzRu9Up2_h5Fno5U7EZRil8AYXKq_9b6fvNsKGxtOGBizg&_tp=eyJjb250ZXh0Ijp7ImZpcnN0UGFnZSI6Il9kaXJlY3QiLCJwYWdlIjoicHJvZmlsZSIsInByZXZpb3VzUGFnZSI6InByb2ZpbGUiLCJwb3NpdGlvbiI6InBhZ2VDb250ZW50In19" target="_blank" class="btn-link" rel="noopener noreferrer">Download</a>
        </article>

        <article>
          <h2>The Role of Artificial Intelligence in Driving ROl through Synergized HR, Marketing, and Financial Decision-Making</h2>
          <div class="authors-journal">
            F Aziz, F Muzaffar, S Shahid, HS Ahmed, SM Iqbal<br />
            Inverge Journal of Social Sciences 4 (3), 129-142, 2025
          </div>
          <a href="https://doi.org/10.63544/ijss.v4i3.153" target="_blank" class="btn-link" rel="noopener noreferrer">DOI</a>
          <a href="https://www.researchgate.net/publication/394366080_The_Role_of_Artificial_Intelligence_in_Driving_ROI_through_Synergized_HR_Marketing_and_Financial_Decision-Making?_tp=eyJjb250ZXh0Ijp7ImZpcnN0UGFnZSI6InByb2ZpbGUiLCJwYWdlIjoicHJvZmlsZSJ9fQ" target="_blank" class="btn-link" rel="noopener noreferrer">ResearchGate</a>
        </article>

        <article>
          <h2>The Strategic Role of Bitcoin in Asset Allocation: Implications for Risk Management and Long-Term Investment Performance</h2>
          <div class="authors-journal">
            A Haidar, F Aziz, I Khan, M Ashfaque, A Hussain<br />
            Journal of Management & Social Science 2 (3), 271-288, 2025
          </div>
          <a href="https://doi.org/10.63075/2at5qa32" target="_blank" class="btn-link" rel="noopener noreferrer">DOI</a>
          <a href="https://www.researchgate.net/publication/394331619_The_Strategic_Role_of_Bitcoin_in_Asset_Allocation_Implications_for_Risk_Management_and_Long-Term_Investment_Performance?_tp=eyJjb250ZXh0Ijp7ImZpcnN0UGFnZSI6InByb2ZpbGUiLCJwYWdlIjoicHJvZmlsZSJ9fQ" target="_blank" class="btn-link" rel="noopener noreferrer">ResearchGate</a>
        </article>

        <article>
          <h2>Lean Assessment of Manufacturing Setup Case Study: Heavy Mechanical Complex Hydraulic Shop, Pakistan</h2>
          <div class="authors-journal">
            FA Shah, A Ramzan, MF Aziz, F Aziz<br />
            International Journal of Advances in Engineering and Management (IJAEM), 2020
          </div>
          <a href="https://www.researchgate.net/publication/394407431_Lean_Assessment_of_Manufacturing_Setup_Case_Study_Heavy_Mechanical_Complex_Hydraulic_shop_Pakistan" target="_blank" class="btn-link" rel="noopener noreferrer">ResearchGate</a>
        </article>

        <article>
          <h2>The Role of Incentive-Based Compensation in Enhancing Sales Team Motivation, Brand Expansion, and Profitability</h2>
          <div class="authors-journal">
            FAziz, R.A Khoso, S Hussain, M Ashfaque<br />
            Research Journal for Social Affairs, 3(5), 529-539, 2025
          </div>
          <a href="https://doi.org/10.71317/RJSA.003.05.0347" target="_blank" class="btn-link" rel="noopener noreferrer">DOI</a>
        </article>

        <article>
          <h2>An Integrated Model for Forecasting Cotton Production, Domestic Consumption, Growth Rate, Area Harvested, Exports and Imports in Pakistan Up to 2050</h2>
          <div class="authors-journal">
            FA Shah, F Aziz, AH Shah, AL Hashmi<br />
            International Research Journal of Modernization, 2020
          </div>
          <a href="https://www.researchgate.net/publication/394407274_AN_INTEGRATED_MODEL_FOR_FORECASTING_COTTON_PRODUCTION_DOMESTIC_CONSUMPTION_GROWTH_RATE_AREA_HARVESTED_EXPORTS_AND_IMPORTS_IN_PAKISTAN_UP_TO_2050" target="_blank" class="btn-link" rel="noopener noreferrer">Download</a>
        </article>

        <article>
          <h2>Influence of glass fibers on mechanical properties of self-compacted concrete</h2>
          <div class="authors-journal">
            F Aziz<br />
            UET Lahore, 2018
          </div>
        </article>
      </section>

      <!-- Supervisors Section -->
      <div class="section-heading">Supervisors</div>

      <div class="person-info">
        <div class="person-name">Professor Jian-Jun Wang</div>
        <div>Dalian University Of Technology, China</div>
        <div>
          <a href="https://scholar.google.com/citations?user=emCIT3sAAAAJ&hl=en" target="_blank" rel="noopener noreferrer">Google Scholar</a>
          <a href="https://www.researchgate.net/profile/Jian-Jun-Wang-2" target="_blank" rel="noopener noreferrer">ResearchGate</a>
          <a href="https://faculty.dlut.edu.cn/leowang/en/index.htm" target="_blank" rel="noopener noreferrer">
