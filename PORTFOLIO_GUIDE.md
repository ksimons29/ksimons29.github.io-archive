# Portfolio Content Guide

This guide shows you how to add and customize content in your portfolio.

## How to Add Content

All content is managed in `_config.yml`. Each section follows the same pattern:

```yaml
content:
  - title: Section Name
    layout: list  # or 'text'
    content:
      # Your items here
```

---

## Adding More Projects to Selected Work

Copy this template and paste it into the `Selected Work` section in `_config.yml`:

```yaml
      - layout: top-middle
        title: [Project Name]
        sub_title: [Your Role] | [Company/Industry]
        caption: [Year] | [Duration]
        description: |
          **Challenge:** [What problem were you solving? 1-2 sentences]

          **Approach:**
          - [Key action 1]
          - [Key action 2]
          - [Key action 3]
          - [Key action 4]

          **Outcome:**
          - [Quantified result 1]
          - [Quantified result 2]
          - [Quantified result 3]
```

### Example - E-commerce Personalization Project

```yaml
      - layout: top-middle
        title: E-commerce Personalization Engine
        sub_title: Senior Product Manager | Retail Tech
        caption: 2021-2022 | 10 months
        description: |
          **Challenge:** Generic product recommendations leading to 2% conversion rates.

          **Approach:**
          - Analyzed 500K user sessions to identify behavior patterns
          - Designed ML-based recommendation algorithm with data science team
          - Built A/B testing framework for continuous optimization
          - Created personalization rules engine for merchandising team

          **Outcome:**
          - Conversion rate increased 2% → 4.5%
          - Average order value up 25%
          - 3x ROI within first 6 months
```

---

## Adding New Sections

### Education Section

Add this after your "Skills" section:

```yaml
  - title: Education
    layout: list
    content:
      - layout: top-middle
        title: [Degree Name]
        sub_title: [University Name]
        caption: [Year Range]
        description: |
          [Optional description, honors, relevant coursework, thesis, etc.]
```

**Example:**

```yaml
  - title: Education
    layout: list
    content:
      - layout: top-middle
        title: Master of Business Administration (MBA)
        sub_title: INSEAD, Fontainebleau
        caption: 2019-2020
        description: |
          Focus on Technology Strategy and Digital Transformation

          - Dean's List
          - Led Product Management Club
          - Capstone: SaaS pricing optimization framework

      - layout: top-middle
        title: BSc Computer Science
        sub_title: University of Cape Town
        caption: 2012-2015
        description: |
          Graduated with Distinction
```

---

### Certifications Section

```yaml
  - title: Certifications
    layout: text
    content: |
      **Product Management**
      - Carnegie Mellon Advanced Product Management (2025)
      - Pragmatic Institute Certified (PMC-VI)
      - Product-Led Growth Certified

      **Technical**
      - AWS Certified Solutions Architect Associate
      - Google Analytics Individual Qualification
```

---

### Speaking & Publications Section

```yaml
  - title: Speaking & Publications
    layout: list
    content:
      - layout: top-middle
        title: "Building AI Products Users Trust"
        sub_title: Speaker | Product Conference Lisbon
        caption: March 2024
        description: |
          Presented framework for responsible AI product development to 300+ PMs.
          [Link to slides](https://example.com)

      - layout: top-middle
        title: "The PM's Guide to Data Governance"
        sub_title: Article | Medium
        caption: January 2024
        description: |
          Deep dive on implementing federated data governance in B2B products.
          5,000+ reads, featured in product management newsletter.
```

---

### Awards & Recognition Section

```yaml
  - title: Awards & Recognition
    layout: text
    content: |
      - **Product Team of the Year** - Company Excellence Awards (2023)
      - **Innovation Award** - Internal hackathon winner for AI prototype (2022)
      - **40 Under 40 PMs to Watch** - Product Management Today (2021)
```

---

## Layout Options

The theme supports different layouts:

### 1. `layout: list` with `layout: top-middle`
Best for: Projects, jobs, education
- Title at top
- Content centered
- Clean, scannable

### 2. `layout: list` with `layout: left`
Best for: When you want image/icon on left
- Content flows right
- Good for logos

### 3. `layout: text`
Best for: Skills, interests, short lists
- Simple text block
- Supports markdown
- No card structure

---

## Adding Links

### Link to Project

```yaml
      - layout: top-middle
        title: Project Name
        link: https://example.com
        link_text: View Live Product
        description: |
          Your project description...
```

### Additional Links (GitHub, etc.)

```yaml
      - layout: top-middle
        title: Open Source Contribution
        additional_links:
          - title: GitHub Repository
            icon: fab fa-github
            url: https://github.com/username/project
          - title: Documentation
            icon: fas fa-book
            url: https://docs.example.com
        description: |
          Your contribution details...
```

---

## Adding Social Links

In the main section of `_config.yml` (not under `content:`), add:

```yaml
# Social links
linkedin_username: koossimons
twitter_username: your_handle
github_username: ksimons29
instagram_username: your_handle
```

Available options:
- `twitter_username`
- `github_username`
- `stackoverflow_username`
- `dribbble_username`
- `facebook_username`
- `flickr_username`
- `instagram_username`
- `xing_username`
- `pinterest_username`
- `youtube_username`
- `orcid_username`
- `googlescholar_username`

---

## Custom Styling Tips

The CSS is in `/assets/css/custom.css`. Here are common customizations:

### Change Primary Color

```css
:root {
  --primary: #1a5f7a;  /* Change this to your color */
  --accent: #d4874b;   /* Change this to your accent */
}
```

### Adjust Card Spacing

```css
.layout, .project-card, article {
  padding: 2rem;  /* Increase for more space */
  margin-bottom: 2rem;  /* Space between cards */
}
```

### Change Fonts

```css
@import url('https://fonts.googleapis.com/css2?family=YourFont&display=swap');

body {
  font-family: 'YourFont', sans-serif;
}
```

---

## Complete Example: Adding Everything

Here's how your full `content:` section might look with all additions:

```yaml
content:
  - title: Selected Work
    layout: list
    content:
      # ... your existing projects ...

      # NEW PROJECT PLACEHOLDER
      - layout: top-middle
        title: [New Project Name]
        sub_title: [Role] | [Company]
        caption: [Year] | [Duration]
        description: |
          **Challenge:** [Problem]

          **Approach:**
          - [Action 1]
          - [Action 2]

          **Outcome:**
          - [Result 1]
          - [Result 2]

  - title: Experience
    layout: list
    content:
      - layout: top-middle
        title: Senior Product Manager
        sub_title: Tech Company Name
        caption: 2020 - Present
        description: |
          Leading product strategy for B2B SaaS platform serving 10K+ users.

          - Own roadmap and vision for data analytics product suite
          - Manage $2M product budget
          - Lead team of 8 engineers and 1 designer

  - title: Education
    layout: list
    content:
      - layout: top-middle
        title: MBA
        sub_title: Business School Name
        caption: 2018-2019
        description: |
          Focus on Technology Management

  - title: Current Learning
    layout: text
    content: |
      **Carnegie Mellon Advanced Product Management Program** (2025)
      Structured PM curriculum covering discovery, roadmapping, and metrics.

  - title: Skills
    layout: text
    content: |
      **Product Management:** Discovery • Roadmapping • Prioritization • Metrics •
      Stakeholder Alignment • Cross-functional Leadership • User Research

      **Technical:** SQL • Power BI • Tableau • Jira • Azure DevOps • Confluence

      **Domains:** Data Products • AI Products • B2B SaaS

  - title: Certifications
    layout: text
    content: |
      - Certification Name (Year)
      - Another Certification (Year)

  - title: Interests
    layout: text
    content: |
      Board member and saxophonist in a big band • Family toy shop digital marketing •
      Camino de Santiago • Music and conversations
```

---

## Testing Your Changes

1. Edit `_config.yml`
2. Commit: `git add _config.yml && git commit -m "Add new section"`
3. Push: `git push`
4. Wait 2-3 minutes for GitHub Pages to rebuild
5. Check https://ksimons29.github.io/

---

## Tips for Great Content

**Projects:**
- Lead with the business problem, not the solution
- Use specific metrics (30% faster, not "much faster")
- Focus on outcomes, not just activities
- 3-4 projects is ideal (quality over quantity)

**Skills:**
- Group by category (PM, Technical, Domain)
- Use bullet separators (•) for visual appeal
- Keep to 3-4 items per category

**About:**
- Lead with your value proposition
- Include location and work preferences
- Keep to 2-3 short paragraphs

---

## Need Help?

- Theme documentation: https://github.com/sproogen/modern-resume-theme
- Markdown guide: https://www.markdownguide.org/
- Font Awesome icons: https://fontawesome.com/icons
