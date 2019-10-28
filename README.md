# iOS PT 3 Demo Day

## Requirements

1. Fork and clone the repository
2. Create a pull request (PR) and tag your TL and instructor

**Add your:**

1. Slide deck (4 required slides in Keynote)
2. Add your links
3. Answer all the questions (Replace placeholders with your answers)
4. Video demo (2 minutes max), share YouTube video link

The video demo is for sharing your work on your portfolio, but it is also a fallback if you have a technical issue during demo time.

## Links (Add your links)

* Code: `<https://github.com/LambdaSchool/ios-pt3-bw1-mortgage-calculator-alex-christian>`
* Trello/Github Project Kanban: `<insert trello board here>`
* Test Flight: `<insert beta signup link here>`  //We were not added into the Lambda's list for TestFlight.
* YouTube demo video: `https://www.youtube.com/watch?v=qzG57EYtHT0&feature=youtu.be>`

## Questions (Answer indented below)

1. What was your favorite feature to implement? Why?

`The whole app was very fun to build for us, but we think that the most fun part was creating both calculators.`

2. What was your #1 obstacle or bug that you fixed? How did you fix it?

`We had different obstacles throughout the entire process but, I think the most difficult we had was constraints.`
  
3. Share a chunk of code (or file) you're proud of and explain why.

   import UIKit
   import WebKit

   class BrowserViewController: UIViewController, WKNavigationDelegate {
       
       @IBOutlet weak var webKitView: WKWebView!
       
       

       override func viewDidLoad() {
           super.viewDidLoad()
           
           webKitView.navigationDelegate = self
           
           navigationItem.rightBarButtonItem = UIBarButtonItem(title: "Home Search Options", style: .plain, target: self, action: #selector(openTapped))

           let url = URL(string:"https://Realtor.com")!
           webKitView.load(URLRequest(url: url))
           webKitView.allowsBackForwardNavigationGestures = true
       }
       
       @objc func openTapped() {
           let ac = UIAlertController(title: "Open Page", message: nil, preferredStyle: .actionSheet)
           ac.addAction(UIAlertAction(title: "Google.com", style: .default, handler: openPage))
           ac.addAction(UIAlertAction(title: "Realtor.com", style: .default, handler: openPage))
           ac.addAction(UIAlertAction(title: "Trulia.com", style: .default, handler: openPage))
           ac.addAction(UIAlertAction(title: "Zillow.com", style: .default, handler: openPage))
           ac.addAction(UIAlertAction(title: "Cancel", style: .cancel))
           ac.popoverPresentationController?.barButtonItem = navigationItem.rightBarButtonItem
           present(ac, animated: true)
       }
       
       func openPage(action: UIAlertAction) {
           guard let actionTitle = action.title else {return}
           guard let url = URL(string: "https://" + actionTitle) else {return}
           webKitView.load(URLRequest(url: url))
           
       }
      
       func webView(_ webView: WKWebView, didFinish navigation: WKNavigation!) {
           title = webView.title
       }

   }
   This code was written to make the Web browser possible.    
    
  
4. What is your elevator pitch? (30 second description your Grandma or a 5-year old would understand)

`How about if I told you that there's an app in the market that will inform you and guide you on the process of getting the house of your dream? Let me tell you all about it...`
  
5. What is your #1 feature?

`The first value is our interest of informing our users how the process work and what to expect from it. The entire app works as one essential step before buying a house.`
  
6. What are you future goals?

`Being able to add more useful features to the app so it can be used by many users in the future.`

## Required Slides (Add your Keynote to your PR)

1. App Name / Team Slide
2. Elevator Pitch
3. Your #1 Feature (Customer facing — what can I do with your app?)
4. Future Goals

## Slide Requirements

1. 50 pt font minimum
2. Be concise — don't write sentences/paragraphs (put these in your slide notes for speaking)
3. 3-6 bullets maximum per slide
4. Do the squint test (can you read the text if you squint, if so, make the font bigger)
6. Images are always welcome
7. Do the Grandma Test (Would your Grandma understand you?)

### Optional Slides

1. Blooper: What's a funny bug or blooper? (screenshots/GIFs please)
2. Revenue Model: If the app was your sole source of income, how would you monetize it?

## Presentation Format

**7 minutes/team**

* 4 minute presentation (5 minute hard cap)
* 3 minutes of questions

We have ~12 teams presenting today — please practice your presentation with a timer (as a team), and make sure you fit within the time limit.

Plan on having one person present the slides and live demo. Please practice your presentation in front of a mirror or with your team 2-5 times. Have the app running and visible in QuickTime so you can quickly transition between slides and live demo.

* App Name / Team Slide (30 seconds)
* Elevator Pitch Slide (30 seconds)
* Your #1 Feature (30 seconds)
* Live Demo (2 minutes)
* Future Goals (30 seconds)
* Questions (3 minutes)

## Final Schedule

### 5th Day

* **Deadline**: 6pm Pacific Code Freeze: Submit your final PR
	* Required: Submit your final TestFlight MVP
* 6pm - 9pm Demo Day Prep and Help (or whenever your usual 5th day hours are)

### Monday

* **Deadline**: 5pm Pacific Submit your Slides (iOS Demo Day PR)
* Required: **iOS Demo Day @ 6pm Pacific** (You must present to complete build week)

