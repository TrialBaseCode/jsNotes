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
- write whole eventlisterner code inside the addEventlistner
  
        document.addEventListener('DOMContentLoaded', function () { });

  and put the all eventlistner in if() only

          if(document.getElementById("rollingBtn")){
        
            let letOne = document.getElementById("letOne");
            let letTwo = document.getElementById("letTwo");
            let rollingBtn = document.getElementById("rollingBtn");
            let textWrk = document.querySelectorAll(".dsbord");
        
            let sidebarContainer = document.querySelectorAll(".sidebar-container");
            rollingBtn.addEventListener("click", toggleClasses);
        
            function toggleClasses(e) {
                e.preventDefault();
                letOne.classList.toggle("col-md-3");
                letTwo.classList.toggle("col-md-9");
                letOne.classList.toggle("col-md-1");
                letTwo.classList.toggle("col-md-11");
                
                textWrk.forEach((element) => {
                    element.classList.toggle("newdisAct");
                });
                
                sidebarContainer.forEach((elem) => {
                    elem.classList.toggle("isecontain");
                });
                // Add CSS transitions outside the loop
                letOne.style.transition = "0.07s linear";
                letTwo.style.transition = "0.07s linear";
            }
        }
        
        if(document.getElementById("imgformFile")){
          // for image file------------------------------------------------
            let imgUpload = document.getElementById("imgformFile");
            imgUpload.addEventListener("change", allChangeImag);
        
            function allChangeImag(e){
                e.preventDefault();
                const [file] = imgUpload.files;
                imageneed.src = URL.createObjectURL(file);
            }
        }

        
