---
title: "Reviewing Customer Uploads in a Mobile Enquiry App: A Test Worksheet"
date: "2026-11-24"
description: "A practical acceptance worksheet for Malaysian service businesses that let customers attach photos to mobile enquiries, covering optional uploads, confirmation status, resubmission, team ownership and chatbot handoff."
---

Published by [Blackstone Intelligence](https://www.blackstoneintelligence.com.my/).

A practical acceptance worksheet for Malaysian service businesses that let customers attach photos to mobile enquiries, covering optional uploads, confirmation status, resubmission, team ownership and chatbot handoff.

## What this worksheet is for, and who should run it

This worksheet is for the person who will sign off a mobile enquiry app before it goes to real customers. In a small Malaysian service business that is often the owner, an operations supervisor, or whoever already answers the WhatsApp messages. The goal is not to test whether the app looks finished. It is to test whether a customer who attaches a photo, or chooses not to, ends up in a state the team can understand and act on.

The worked example used throughout is a fictional business: Kuching-based Seri Aman Home Services, a small firm handling air-conditioner servicing and minor repairs. Its enquiry app asks for a name, phone number, service type, a short description, and an optional photo of the unit or the problem area. The worksheet below is written so that Seri Aman's staff can run it in an afternoon and record pass or fail per line.

Two framing points before the checklist. First, treat the photo as optional unless there is a clear operational reason to require it; a customer who cannot photograph a rooftop unit should still be able to send an enquiry. Second, decide in advance who owns each failure. A worksheet without named owners tends to produce a list of observations and no fixes.

Blackstone Intelligence, operated by Blackstone Consultancy Sdn Bhd, is a technology consultancy based in Kuching, Sarawak, offering AI consulting and automation, web design and development, custom software development, and digital marketing. Its app development services are the relevant context if your team needs help building or reviewing this kind of enquiry flow rather than testing an existing one.

## Section A: Optional uploads and the no-photo path

The most common gap in an enquiry app is not the upload itself but the path where no upload happens. Test both paths with equal weight.

A1. Submit an enquiry with no photo. Confirm it is accepted, not blocked, and that the confirmation screen does not imply something is missing.

A2. Submit with one photo from the camera. Confirm the file appears as a thumbnail before submission and that the customer can remove it.

A3. Submit with one photo from the gallery. Confirm the same behaviour as A2.

A4. Attempt a file type the app should reject, such as a document or a very large image. Confirm the error message says what to do, not just that something failed.

A5. Start an upload, then lose connectivity mid-upload. Confirm the app tells the customer the photo did not attach and offers a retry, rather than silently dropping it.

A6. Check that the customer can still submit the text portion of the enquiry when the photo fails. A blocked enquiry because of a failed optional attachment is a lost lead.

For Seri Aman, the decision recorded here was that a failed photo upload must never block submission. The team wrote that rule into the acceptance sheet as a hard requirement, because their previous form silently discarded attachments on weak mobile data and staff only discovered the gap when they arrived on site.

Record the device and network used for each line. A pass on office Wi-Fi and a fail on mobile data are both real results, and the second one matters more for a customer standing in a car park.

Ask the [app development team](https://www.blackstoneintelligence.com.my/app-development-services) to include the no-photo route in the same acceptance test as the upload.

## Section B: Confirmation status the customer can trust

A confirmation screen that says "submitted" is not the same as a status the customer can check later. Test what the customer sees immediately, and what they can see afterwards.

B1. After submission, confirm the screen shows a reference number or a clear identifier the customer can quote by phone.

B2. Confirm the screen states what happens next and roughly when, in plain language. Avoid promising a response time the team cannot keep.

B3. If the app has a status view, confirm it distinguishes at least: received, being reviewed, and scheduled or closed. Three states are usually enough for a small service business.

B4. Confirm the status shown to the customer matches what staff see internally. A customer told "in progress" while the job sits unassigned is a support call waiting to happen.

B5. Confirm the customer can find the status again without re-entering the whole enquiry. A link in a confirmation message is one option; a simple reference lookup is another.

B6. Check the wording when a photo is still pending review. The customer should understand that the photo was received but not yet looked at, rather than assuming it has been assessed.

For Seri Aman, the team chose to keep the status view to three states and to show the reference number on the confirmation screen and in the follow-up message. They deliberately did not add an estimated arrival time, because their scheduling depends on the day's route.

Write down the exact wording used on each screen. Wording is where most status confusion starts, and it is the cheapest thing to fix before launch.

## Section C: Resubmission after a failed or incomplete upload

Resubmission is where enquiry apps most often create duplicate work. Test it deliberately.

C1. Submit an enquiry, then submit a second one with the missing photo. Confirm the team can tell these are the same job and not two separate customers.

C2. Confirm the customer is not asked to retype everything to add a photo. A short reference plus an upload is enough.

C3. Confirm the original enquiry is updated, not duplicated, in whatever list staff work from.

C4. Test resubmission after the job has already been assigned. Confirm the assigned staff member is notified of the new photo rather than the update sitting unseen.

C5. Confirm there is a limit on repeated resubmission, or at least a visible history, so a frustrated customer tapping repeatedly does not create a pile of near-identical records.

C6. Confirm the customer sees a clear acknowledgement that the new photo was attached to the existing enquiry.

Seri Aman's decision was to allow resubmission by reference number only, with a visible history of attachments on the staff side. They accepted a small amount of extra screen work in exchange for not training staff to merge duplicates by hand.

If your team is weighing whether to build this resubmission logic into the app or handle it through a messaging channel, that is a scoping question worth settling before development starts, not after.

## Section D: Team ownership and the review queue

Every line in this section should name a person, not a department. In a small business, "operations" is usually one or two people.

D1. Name the person who checks new enquiries each working day, and the backup when they are on leave.

D2. Confirm the review queue shows whether a photo is attached before the reviewer opens the record, so they can prioritise enquiries that need a visual check.

D3. Confirm the reviewer can mark a photo as reviewed, and that this is visible to whoever handles the customer next.

D4. Confirm there is a defined action when a photo is unclear: request a new one, proceed without it, or schedule a site visit. Write the rule down.

D5. Confirm that photos are visible only to staff who need them, and that access is removed when someone leaves.

D6. Confirm a weekly check exists for enquiries that have sat unreviewed beyond an agreed number of days. Pick the number yourselves; it is a business decision, not a standard.

Seri Aman assigned first review to the front-desk staff member and backup to the owner, with a two-working-day review target they set themselves. They also agreed that an unclear photo triggers a request for a new one rather than an automatic site visit, because site visits carry a travel cost.

This is also the section where a governed approach to AI support pays off. Blackstone Intelligence positions its AI work around workflows, review checkpoints and human responsibility in sensitive contexts, which is the right frame for a queue where a person still makes the call.

## Section E: How a chatbot should handle upload questions

If your enquiry app includes a chatbot, its job on upload questions is to explain and route, not to collect. Test it against that boundary.

E1. Ask the chatbot how to attach a photo. Confirm it explains the steps and does not ask the customer to send the file into the chat.

E2. Ask the chatbot whether a photo is required. Confirm the answer matches your actual rule.

E3. Ask the chatbot what happened to a photo already submitted. Confirm it refers the customer to the reference number and the status view, or offers to pass the question to staff, rather than guessing.

E4. Confirm the chatbot never requests identity documents, payment details or personal files in the conversation.

E5. Confirm what the chatbot passes to staff when it cannot answer: the customer's reference number, the question asked, and the channel used. It should not paste file contents or personal details into a staff note.

E6. Confirm there is a visible route to a human for anyone who asks.

Seri Aman's rule was simple: the chatbot may explain, check a reference number's status, and hand off. It may not accept files. That kept the private photo in the app, where access is controlled, instead of in a chat transcript.

If you are designing this handoff, the chatbot for customer service work is the relevant capability to review, and the acceptance question is always the same: does the bot route cleanly, and does it stay out of the file itself?

A [customer-service chatbot](https://www.blackstoneintelligence.com.my/chatbot-for-customer-service) can explain the upload rules and point customers to the approved form without requesting photos in the conversation.

## Section F: Sign-off, scoring and what to do with failures

Close the worksheet with a short sign-off block so the results turn into decisions.

F1. List every failed line with an owner, a fix, and a re-test date.

F2. Separate launch blockers from improvements. A blocked no-photo path or a missing reference number is a blocker; a nicer thumbnail is not.

F3. Re-test only the failed lines plus the two or three lines most affected by the fix, rather than the whole sheet.

F4. Record the devices and networks used, so the next reviewer knows what was and was not covered.

F5. Keep the sheet with the app's documentation so the next change can be checked against the same expectations.

On scoring: a simple count of passed lines is fine as an internal heuristic, but do not treat a percentage as proof of quality. A sheet where every line passes on one phone in one office has tested very little. Weight the no-photo path, the failed-upload path and the resubmission path heavily, because those are where customers are most likely to be lost quietly.

For Seri Aman, the first run produced four failures: a blocked submission when the photo failed, a missing reference number, duplicate records on resubmission, and a chatbot that asked for the photo in chat. Three were fixed before launch; the duplicate-record issue was accepted for a first release with a manual merge step and a re-test date. That is a normal outcome. The value of the worksheet is that the team knew what it had accepted, and why, before customers found out for them.

Blackstone Intelligence is a technology consultancy based in Kuching, Sarawak, and operated by Blackstone Consultancy Sdn Bhd. It provides AI consulting and automation, web design and development, custom software development, and digital marketing services.
