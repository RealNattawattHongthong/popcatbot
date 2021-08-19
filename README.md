// Bot for popcat 
// ก็อปตรงข้างบนได้เลย ไม่มีผลกับการทำงาน
// กับแบน แบบ auto
//Make By Nattawatt Hongthong 
//ถ้าเหมือนใครก็ขอโทษด้วยนะ
//link https://treenattawatt.web.app/
//IG nattawatthongthong
//Facebook Nattawatt Hongthong
const kbd = new KeyboardEvent('keydown',{
    key:'h',
    ctrlKey:'true'
});
const kbu = new KeyboardEvent('keyup',{
    key:'h',
    ctrlKey:'true'
});
function getCookie(cname) {
    let name = cname + "=";
    let decodedCookie = decodeURIComponent(document.cookie);
    let ca = decodedCookie.split(';');
    for(let i = 0; i <ca.length; i++) {
      let c = ca[i];
      while (c.charAt(0) == ' ') {
        c = c.substring(1);
      }
      if (c.indexOf(name) == 0) {
        return c.substring(name.length, c.length);
      }
    }
    return "";
  }
function checkCookie() {
    let isbot = getCookie("bot");
    if (isbot != "") {
        console.log("Ban Detected! Clearing..")
        document.cookie = "bot=; expires=Thu, 01 Jan 1970 00:00:00 UTC; path=/;";
    }
}
const x = setInterval(function(){
    checkCookie();
    document.dispatchEvent(kbd);
    document.dispatchEvent(kbu);
    //console.log("clicked")
},40);
