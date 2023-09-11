# for toggle the sidebar----------------------------

    const letOne = document.getElementById("letOne");
    const letTwo = document.getElementById("letTwo");
    const rollingBtn = document.getElementById("rollingBtn");
    const textWrk = document.querySelectorAll(".dsbord");
    
    rollingBtn.addEventListener("click", toggleClasses);
    
    function toggleClasses() {
        letOne.classList.toggle("col-md-3");
        letTwo.classList.toggle("col-md-9");
        letOne.classList.toggle("col-md-1");
        letTwo.classList.toggle("col-md-11");
    
        textWrk.forEach((element) => {
            element.classList.toggle("newdisAct");
        });
    
        // Add CSS transitions outside the loop
        letOne.style.transition = "width 0.08s linear";
        letTwo.style.transition = "width 0.08s linear";
    }

//------------------------

    const letOne = document.getElementById("letOne");
    const letTwo = document.getElementById("letTwo");
    const rollingBtn = document.getElementById("rollingBtn");
    const textWrk = document.querySelectorAll(".dsbord");
    
    rollingBtn.addEventListener("click", toggleClasses);
    
    function toggleClasses() {
        letOne.classList.toggle("col-md-3");
        letTwo.classList.toggle("col-md-9");
        letOne.classList.toggle("col-md-1");
        letTwo.classList.toggle("col-md-11");
    
        textWrk.forEach((element) => {
            element.classList.toggle("newdisAct");
        });
    
        // Add CSS transitions outside the loop
        letOne.style.transition = "width 0.08s linear";
        letTwo.style.transition = "width 0.08s linear";
}

## Notes 
- for using class name tag use in classlist we have to use array or for loop. => document.getElementsClassName();
- If you need to classlist to work then using document.getElementById();

# Eventlistern problem to solve
- when error come "Cannot read property 'addEventListener' of null"
  
    document.addEventListener('DOMContentLoaded', function () { });
