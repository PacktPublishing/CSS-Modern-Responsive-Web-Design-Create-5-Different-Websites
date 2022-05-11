const toggler = document.querySelector('.toggle');
const navbar = document.querySelector('.navbar');
const navItems = document.querySelectorAll('.navItem');
console.log(navItems);

navItems.forEach((ele)=>{
    console.log(ele);
    if(ele.querySelector('.subNav')){
        ele.addEventListener('click',(e)=>{
            if(ele.classList.contains('sactive')){
                ele.classList.remove('sactive');
            }else{
                ele.classList.add('sactive');
             }   
        })
    }
})


toggler.addEventListener('click',(e)=>{
    if(navbar.classList.contains('active')){
        navbar.classList.remove('active');
        toggler.querySelector('a').innerHTML = '<i class="fas fa-bars"></i>';
    }else{
        navbar.classList.add('active');
        toggler.querySelector('a').innerHTML = '<i class="fas fa-window-close"></i>';
    }
})