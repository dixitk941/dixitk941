Certainly! Here's your profile with the added website links and the GitHub API integration for the charts:

---

### Hello there! 👋 I'm Dixitk941.

I am a diligent BCA student at Rajiv Academy of Technology and Management, deeply passionate about coding and web development. Currently, I am actively engaged in exploring diverse facets of the tech world and endeavoring to construct intriguing projects.

- 🔭 **Currently Working On:** I'm focused on developing web applications and advancing my coding proficiency.
- 🌱 **Currently Learning:** I'm dedicated to exploring new technologies and frameworks to augment my development skills.
- 👯 **Seeking Collaborations In:** Open source projects, web development, and any intellectually stimulating endeavors!
- 💬 **Ask Me About:** Web development, coding, or any tech-related queries. I'm here to assist!
- 📫 **How to Reach Me:** 
  - **Instagram:** [karan_dixit19](https://www.instagram.com/karan_dixit19/)
  - **LinkedIn:** [Karan Dixit](https://www.linkedin.com/in/karan-dixit-7223a628a/)
  
**Noteworthy Projects:**
- [Paris Spices Website](https://www.parisspices.com)
- [Hitown Bears Website](https://hitownbears.live)
- [My Portfolio](https://dixitk941.github.io/myportfolio/)
- [ClimateCheck360](https://climatecheck360.vercel.app)
- [GenZConnect](https://genzconnect.vercel.app)

- 😄 **Pronouns:** He/Him
- ⚡ **Fun Fact:** I relish experimenting with new coding challenges and savoring various cuisines from around the globe!

**Coding Activity Charts:**

- **Commits Chart:** 
  ```html
  <div id="commits"></div>
  ```
  
- **Progress Chart:** 
  ```html
  <div id="progress"></div>
  ```


```javascript
// Fetch GitHub Data
fetch('https://api.github.com/users/dixitk941/events')
  .then(response => response.json())
  .then(data => {
    // Filter out the push events
    const pushEvents = data.filter(event => event.type === 'PushEvent');
    
    // Calculate total commits
    const totalCommits = pushEvents.reduce((acc, event) => {
      return acc + event.payload.size;
    }, 0);

    // Display total commits
    document.getElementById('commits').innerText = `Total Commits: ${totalCommits}`;
  })
  .catch(error => {
    console.error('Error fetching GitHub data:', error);
  });
```
