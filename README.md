# Campus Stores

Campus Stores is a Product Engineer work sample set at a fictional campus equipment desk. The Film Society borrows a screening kit on Friday and brings it back in two trips. Open **Candidate brief** in the app for the assignment.

## Run the app

Open `index.html` in a modern browser. The app includes its scripts, styles, and icons and can run offline.

To serve it over local HTTP, run this from the repository folder and visit `http://localhost:8000`.

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

Each browser stores its own sample shift locally when browser storage is available. **Restart sample shift** restores the fictional starting records.

## The decision

I’d keep one slip per physical item. When Kabir brings back projector `PR-04` and speaker `SP-02`, the clerk can put both back on the shelf and leave adapter `AD-12` checked out. The two completed slips are still easy to find under **All slips**.

The handover took more work. The approved request looked the same before pickup and after two items came back. The Loan register showed the adapter and its original Friday 8 pm due time, while Kabir’s Desk book message said Leela would bring it back Saturday at 9 am. The next clerk had to piece those details together to find the right slip.

## What changed

- **The request shows what’s left.** The list shows each request’s progress as the clerk issues and returns items. After the partial return, the Film Society’s request reads **2 of 3 returned · 1 still out**. Open it to see each approved item’s status and the latest unit and slip for items that went out. Earlier slips are in the Loan register under **All slips**.
- **The handover lives on the item’s slip.** The Friday clerk can save **Leela Das · Sat 9 am** on `AD-12`. The next clerk sees who’s bringing the adapter and when, alongside Kabir’s name and the original due time. The plan is still there after a reload.
- **Both screens use the same record.** The clerk can add or edit the handover and record the return in either Requests or the Loan register. Check in `AD-12` from either screen and the request shows **All returned**, the slip closes, and the adapter goes back on the shelf in Inventory.

On narrow screens, a long handover entry could overlap the **Record return** button. The text now wraps inside the item row so the button stays usable.

## Replay the shift

Select **Restart sample shift** to start at Friday pickup.

1. **Friday pickup.** Open **Courtyard screening** in Requests. It starts at **Awaiting pickup**. In the Loan register, issue `PR-04`, `SP-02`, and `AD-12` on separate slips for `RQ-214`, using **Kabir Sen** and **Fri 8 pm** for each. The request shows **All 3 issued**. Select **Move to return time**.
2. **Friday return.** In the Loan register, record the projector and speaker returns. On the remaining adapter slip, select **Add handover**, choose **Leela Das**, enter **Sat 9 am**, and save. Open **Courtyard screening** in Requests to see **2 of 3 returned · 1 still out** and the saved handover. Select **Move to next morning**.
3. **Saturday handover.** With the request open, match the physical label to `AD-12` and select **Record return** on that row. Requests now shows **All returned**. The Loan register also shows the slip as returned under **All slips**.

At a real counter, I’d time how long a clerk who just started their shift takes to identify the correct open slip after an adapter is placed on the counter. I’d compare the original and prototype flows with two similar adapters in stock.

## Source

- `index.html` contains the desk layout, candidate brief, and bundled icons.
- `app.js` contains the sample records and interactions.
- `styles.css` defines the desktop and mobile layouts.

Icon license notices are in [third-party/lucide-LICENSE.txt](third-party/lucide-LICENSE.txt).


## Submit your work

1. [Fork Campus Stores](https://github.com/virinchi-healthcare/campus-stores/fork) into your GitHub account. Complete the candidate brief and push your changes to your public fork. In your README, point reviewers to your work and explain the decision you made.
2. In your fork, open **Commits**, select the final commit you want reviewed, and copy the page URL. It should look like `https://github.com/YOUR-USERNAME/campus-stores/commit/COMMIT-SHA`.
3. [Submit your work through the Google Form](https://docs.google.com/forms/d/e/1FAIpQLScvzoh1R4WS-SkiwAVBQbMvniieJYSoOEfLMyVo5CyjOvYUgQ/viewform). Your **roll number**, **email ID**, and **final commit link from your public fork** are required. Enter your roll number and email ID in the form only.
