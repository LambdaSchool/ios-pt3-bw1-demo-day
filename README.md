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

* Code: `<https://github.com/LambdaSchool/ios-pt3-bw1-mortgage-calculator-craig-gavin>`
* Trello/Github Project Kanban: `<insert trello board here>`
* Test Flight: `<insert beta signup link here>`
* YouTube demo video: `<https://youtu.be/DgoPtdj5qj8>`
* Keynote slides: `<https://www.icloud.com/keynote/06AIhtEulsccxSA0QX8FNnB6A#Palm_Mortgage>` 

## Questions (Answer indented below)

1. What was your favorite feature to implement? Why?

    `<We really enjoyed getting the view controllers to communicate with each other.  That included some prepare for segues and delegates, and even adding a variable that we overlooked.  It was enjoyable because of how challenging it was, and the satisfaction that came from seeing it work!>`

2. What was your #1 obstacle or bug that you fixed? How did you fix it?

    `<Tough to choose just one.  But I suppose we’d go with the issue we ran into with the keyboard blocking some of our text input fields.  We brainstormed how to fix it, and thought a scroll view would be best.  However, due to lack of time and familiarity we went with a simpler fix of changing the layout.  These are real world issues, and real world solutions.  Sometimes you just have to make something work to meet a deadline, and that is what we did here.>`
  
3. Share a chunk of code (or file) you're proud of and explain why.

    `<From our LoanLibraryTableViewController:
        override func prepare(for segue: UIStoryboardSegue, sender: Any?) {
            switch segue.identifier {
            case "ModifyLoanFromLibrarySegue":
                    guard let loanCalculatorVC = segue.destination as? LoanCalculatorViewController else { fatalError() }
                    loanCalculatorVC.delegate = self
                    loanCalculatorVC.loanmodelcontroller = loanmodelcontroller
            case "ShowLoanDetailSegue":
                guard let loanDetailVC = segue.destination as? LoanDetailViewController,
                    let loanmodelcontroller = loanmodelcontroller,
                    let indexPath = tableView.indexPathForSelectedRow else { fatalError() }
                loanDetailVC.loan = loanmodelcontroller.loans[indexPath.row]
            default:
                return
            }
        }
        This bit of code had some real team work.  We both had a hand in it.  Craig got it got a 
        good chunk of it done.  Gavin tried implementing the portion dealing with the 
        “ShowLoanDetailSegue”, but got stuck at a point.  Craig was able to go in and take a look
        and help solve it.  Part of the issue was that Gavin had commented out some code that
        prevented him from appending the .loan.  Sometimes it takes a second set of eyes to
        see the solution.>`
  
4. What is your elevator pitch? (30 second description your Grandma or a 5-year old would understand)

    `<To a 5 year old: 
    “Do you like pushing buttons on a phone? Here!”*
    *App not designed for a 5 year old
    But honestly, to our target market:
    “Would you sign on the dotted line of the first loan you were offered?  Our app helps you compare loans and make an educated decision.  It’s easy to overlook how much interest you pay over the entire life of the loan, and often it is tempting to minimize upfront costs and monthly payments; however, if you are able to see how many thousands of dollars that might cost you in the long-run, you may give it a second thought.  See clearly how something like $20 extra per month toward a home mortgage could save you several thousand dollars in additional interest.”>`
  
5. What is your #1 feature?

`<Our #1 feature has to be the ability to compare loans quickly and easily.  You get a quick snapshot in the LoanLibraryTableViewController, and can drill down for more details in the LoanDetailViewController.>`
  
6. What are you future goals?

`<Our goal is to help users make smart, informed decisions.  Based off of that, it’d be nice to have a feature to help show what loan amount you should seek (based off of credit score, income, zip code you live in (to estimate living costs), etc).  That way you can look at a car, a home, or whatever, within you budget.>`

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

