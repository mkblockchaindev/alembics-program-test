## 5 Program Test - Smart contract development
================================================

1: The worst case number of drops are 19
Duration : 10 mins

The problem is to detect the maximum floor which can make PS survivable from drop. The main task is to find out the optimized dropping methods. 
So I decided to divide 100 floors by 10 parts, because 100 = 10 x 10. 

The following is the way
1) I can drop 'A' PS from 10th, and then if it is survivable, do it again from 20th and go on this until 'A' PS is broken. 
2) if 'A' PS is broken from (N+1) * 10 th floor, I will drop 'B' PS from N * 10th floor and if it is survivable, drop it again from N * 10th + 1 floor and repeat it again until 'B' PS is broken
3) if 'B' PS is broken from N * 10th + M floor, The expected floor is N * 10th + M -1 floor

If 99th is survivable maximum floor,  it is worst case number of drops at that time and it is 19.


2: What tools do you use on a day to day basis?
Duration : 3 mins

mailbox : I always start the workday by checking it in the morning.
telegram / slack / skype : This tools are most important for team communications
google meet / zoom meeting : same as above
git : This is repository management tools for work
vscode : This is my preferred text editor for development.
chrome browser: My favourite web browser.

3: What kind of questions will you ask to candidate?
Duration : 3 mins
- Please introduce yourself about your software development career
- How many years do you have as frontend developer?
- Which framework do you like to use for frontend?
- Please let me know your most difficult problem that you met before on the development, let me know it how you could solve it

4: Javascript test
Duration : 10 mins

const Matrix = [2, 3, 4, 8, 5, 7, 9, 12, 1, 0, 6, 10]
console.log(Matrix)

const Result = BuildStringFromMatrix(Matrix, 4, 3)
console.log(Result)

function BuildStringFromMatrix(inMatrixElements, NumRows, NumColumns) {
  let result = [];
  for (let i=0; i < NumRows * NumColumns; i++) {
    const row = (i - i % NumRows) / NumRows;
    const col = row % 2 == 0 ? i % NumRows : NumColumns - i % NumRows;
    // console.log(i + ":[" + row + "," +col + "]");
    result[i] = inMatrixElements[row * NumRows + col];
  }
  return result;
}


// Try other templates: Project -> New


5: Smart contract challenge
5a) 1 min
Answer: D)
*A* and *B* should get their deposit + the corresponding rewards based on the time they have been in the pool

===================
Duration 6), 7) 2hrs
6) Deploy your contract from question 6
Deployed address : 0xb8F62A696d49A3c81883e77Ce339EAC24A30B449
Verified

7) Interact with contract from question 7
craeted interact.js

