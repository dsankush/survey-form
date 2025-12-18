# Client Feedback & Approval Lifecycle Survey Platform

A professional, responsive survey platform for collecting feedback on client feedback and approval processes and their impact on project delivery and stakeholder satisfaction.

## 🎯 Features

- **Professional UI/UX**: Clean, modern design with a light theme
- **Fully Responsive**: Works seamlessly on desktop, tablet, and mobile devices
- **Progress Tracking**: Visual progress bar showing completion status
- **Form Validation**: Built-in validation to ensure all required fields are filled
- **Webhook Integration**: Automatically submits responses to your n8n webhook
- **Smooth Animations**: Interactive elements with smooth transitions
- **Structured Data**: Responses are organized into clear sections for easy analysis

## 📋 Survey Structure

The survey consists of 5 main sections:

### Section A: Demographic Information
- Respondent's name
- Email address
- Current role in organization
- Years of professional experience

### Section B: Client Feedback Efficiency (4 statements)
- Timeliness of feedback
- Clarity and actionability
- Communication effectiveness
- Impact of delays

### Section C: Approval Process Efficiency (4 statements)
- Authority definition
- Multiple approval layers
- Escalation mechanisms
- Process consistency

### Section D: Project Delivery Timeliness (4 statements)
- Schedule adherence
- Impact of approval delays
- Efficiency benefits
- Stakeholder coordination

### Section E: Stakeholder Satisfaction (4 statements)
- Communication satisfaction
- Trust and confidence
- Overall satisfaction
- Long-term relationships

## 🚀 How to Use

### Option 1: Open Directly in Browser
Simply open the `index.html` file in any modern web browser:
```bash
# On Linux/Mac
open index.html

# On Windows
start index.html

# Or double-click the file in your file explorer
```

### Option 2: Serve with a Local Server
For testing or development:

**Using Python:**
```bash
# Python 3
python -m http.server 8000

# Then open: http://localhost:8000
```

**Using Node.js:**
```bash
npx http-server
# Then open the URL shown in terminal
```

**Using PHP:**
```bash
php -S localhost:8000
# Then open: http://localhost:8000
```

## 📤 Webhook Integration

The survey is configured to send responses to:
```
https://n8n.srv1152566.hstgr.cloud/webhook/9ea174cc-7458-463e-adcb-5bedd1d39ed6
```

### Response Format

Responses are sent as JSON with the following structure:

```json
{
  "timestamp": "2025-12-18T10:30:00.000Z",
  "respondent": {
    "name": "John Doe",
    "email": "john.doe@example.com"
  },
  "demographics": {
    "role": "Project Manager",
    "experience": "5–10 years"
  },
  "client_feedback_efficiency": {
    "feedback_timely": 4,
    "feedback_clear": 3,
    "feedback_communicated": 4,
    "feedback_delays_impact": 5
  },
  "approval_process_efficiency": {
    "approval_defined": 4,
    "approval_layers_delay": 3,
    "approval_escalation": 3,
    "approval_consistent": 4
  },
  "project_delivery_timeliness": {
    "delivery_on_schedule": 3,
    "delays_cause_overruns": 4,
    "efficiency_reduces_delays": 5,
    "timely_approvals_coordination": 5
  },
  "stakeholder_satisfaction": {
    "client_communication_satisfaction": 4,
    "feedback_improves_trust": 5,
    "streamlined_approval_satisfaction": 4,
    "process_influences_relationships": 4
  }
}
```

## 🎨 Customization

### Change Webhook URL
Edit line 546 in `index.html`:
```javascript
const WEBHOOK_URL = 'YOUR_NEW_WEBHOOK_URL';
```

### Modify Colors
Update the CSS variables in the `:root` section (lines 14-24):
```css
:root {
    --primary-color: #4f46e5;  /* Main brand color */
    --primary-dark: #4338ca;   /* Darker shade for hover */
    --primary-light: #eef2ff;  /* Light background */
    /* ... more colors */
}
```

### Add Additional Questions
Follow the existing pattern for Likert scale questions or radio groups in the HTML.

## 🔒 Privacy & Security

- All responses are submitted directly to your webhook
- No data is stored locally or by third parties
- HTTPS connection ensures secure data transmission
- Responses are confidential and for academic purposes only

## 📱 Browser Compatibility

- ✅ Chrome/Edge (latest)
- ✅ Firefox (latest)
- ✅ Safari (latest)
- ✅ Mobile browsers (iOS Safari, Chrome Mobile)

## 🛠️ Technical Stack

- **HTML5**: Semantic markup
- **CSS3**: Modern styling with CSS Grid and Flexbox
- **Vanilla JavaScript**: No dependencies required
- **Responsive Design**: Mobile-first approach

## 📊 Data Analysis

The structured JSON format makes it easy to:
- Import into spreadsheet applications (Excel, Google Sheets)
- Analyze with data science tools (Python, R)
- Visualize with BI tools (Power BI, Tableau)
- Process with n8n workflows

## 🤝 Support

For issues or questions about the survey platform, please refer to the documentation or contact the research team.

## 📄 License

This survey is for academic research purposes. All responses will be kept confidential.

---

**Built with ❤️ for academic research**
