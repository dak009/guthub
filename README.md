<!DOCTYPE html>
<html lang="ko">

<head>
   <meta charset="UTF-8">
   <meta name="viewport" content="width=device-width, initial-scale=1.0">
   <title>무학고등학교</title>
   
   <style>
      .nonline{
    border: 0cm;
}
.button{
    height: 50px;
    width: 135px;
    font-size: 30px; 
    font-family:'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
    margin-bottom: 10px;
    border-radius: 3px;
    background-color: rgba(214, 97, 30, 0.605);
}
.button:hover{
    transition: 0s;
    background-color: rgb(254, 173, 107);
}
.pt{
    width: 10px;
    height: 10px;
    object-fit: cover;
}
.hs{
    height: 50px;
    width: 135px; 
    font-size: 30px; 
    font-family:'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
    margin-bottom: 10px;
    border-radius: 3px;
    background-color: rgb(12, 154, 106);
}
.hs:hover{
    transition: 0s;
    background-color: rgb(36, 197, 105);
}
.hs2{
    height: 50px;
    width: 135px;
    font-size: 30px; 
    font-family:'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
    margin-bottom: 10px;
    border-radius: 3px;
    background-color: rgb(70, 104, 197);
}
.hs2:hover{
    transition: 0s;
    background-color: rgb(120, 155, 204);
}
.buttonfinish{ 
   background-color: rgb(241, 91, 91);
   height: 30px; 
   width: 70px; 
   border-radius: 20px;
   font-family:'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
}
.buttonfinish:hover{
   transition: 0s;
   background-color: rgb(255, 0, 0);
}
.left{
    float: left;
}
   </style>
</head>

<body>
   <script src="scripts/자바.js">
    localStorage.setItem("go1", "0");
  </script>
 <div style=" height: 200px; width: 1500px; ">

    <div style="float: left;  height: 200px;  border-radius: 10px;">
      <form action="http://localhost/출석표2.php" method="post" id="myForm">
          <label style="font-size: 20px; font-family:'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;">날짜를 선택하세요:
            <input type="date" name="bday" pattern="\d{4}-\d{2}-\d{2}" style="font-size: 20px; float: right;">
            <span class="validity"></span>
          </label><hr>

          <label style="font-size: 20px; font-family:'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;">출석한 인수를 입력하시오        
              <input type="text" name="userInput_on" style="float: right;">
          </label><hr>

          <label style="font-size: 20px; font-family:'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;">출석하지 않은 인원수를 입력하시오
              <input type="text" name="userInput_off">
          </label><hr>
              <input type="submit" class="buttonfinish" onclick="alert('저장되었습니다')" value="저장하기" style="float: right;">
      </form>

      <div style="float: right;">
          <form action="http://localhost/출석표3.php" method="post">
              <input type="submit" value="출석목록" class="buttonfinish" style="float: right;">
          </form>
      </div>
      <!--
        출석인원확인자리
      -->
    </div>

    <div style="margin-left: 550px; margin-right: 550px; width: 400px; height: 200px; ">
       <h1 style="font-family: Georgia, 'Times New Roman', Times, serif; font-size: 60px;">무학고등학교  </h1>
    </div>

 </div>

 <div style="height: 540px; width: 1500px;">

    <div style="width: 135px;  margin-right: 60px; height: 1150px; float: left;">
        <button class="button" onclick="toggleImg1()">
   
                <div style="float: left;">
                        <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img1" >
                        <script>
                          var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
                          var go1 = localStorage.getItem("go1");
                          console.log(go1);
                          
                          function toggleImg1() {
                          var imgElement = document.getElementById("img1");
                          
                          
                          // 이미지 상태에 따라 토글
                          if (img1Status === "not") {
                              imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                              img1Status = "set"; // 상태 변경
                              go1= go1+1;
                          } else {
                              imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                              img1Status = "not"; // 상태 변경
                              go1=go1-1;
                            }

                          }
                        </script>
                </div>
       
                <div style="float: right; height: 30px;">
                   <h1 style="font-size: 15px; margin: 0px;">
                      1110 박지우
                   </h1>
                </div>
                
             </button>

         
   
         <button class="button" onclick="toggleImg2()">
            <div style="float: left;">
               <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img2">
               <script>
                  var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
              
                  function toggleImg2() {
                      var imgElement = document.getElementById("img2");
              
                      // 이미지 상태에 따라 토글
                      if (img1Status === "not") {
                          imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                          img1Status = "set"; // 상태 변경
                          go1=go1+1;
                      } else {
                          imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                          img1Status = "not"; // 상태 변경
                          go1=go1-1;
                      }
                  }
              </script>
            
            </div>
            <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  1112 서동겸
               </h1>
            </div>
         </button>
      
       <button class="hs" onclick="toggleImg3()">
            <div style="float: left;">
               <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img3">
               <script>
                  var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
              
                  function toggleImg3() {
                      var imgElement = document.getElementById("img3");
              
                      // 이미지 상태에 따라 토글
                      if (img1Status === "not") {
                          imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                          img1Status = "set"; // 상태 변경
                          go1=go1+1;
                      } else {
                          imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                          img1Status = "not"; // 상태 변경
                          go1=go1-1;
                      }
                  }
              </script>
   
            </div>
            <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  1120 정보석
               </h1>
            </div>
         </button>
   
         <button class="hs" onclick="toggleImg4()" >
            <div style="float: left;">
               <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img4">
               <script>
                  var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
              
                  function toggleImg4() {
                      var imgElement = document.getElementById("img4");
              
                      // 이미지 상태에 따라 토글
                      if (img1Status === "not") {
                          imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                          img1Status = "set"; // 상태 변경
                          go1=go1+1;
                      } else {
                          imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                          img1Status = "not"; // 상태 변경
                          go1=go1-1;
                      }
                  }
              </script>
   
            </div>
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  1121 정수환
               </h1>
            </div>
         </button>
   
         <button class="button" onclick="toggleImg5()">
            <div style="float: left;">
               <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img5">
               <script>
                  var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
              
                  function toggleImg5() {
                      var imgElement = document.getElementById("img5");
              
                      // 이미지 상태에 따라 토글
                      if (img1Status === "not") {
                          imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                          img1Status = "set"; // 상태 변경
                          go1=go1+1;
                      } else {
                          imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                          img1Status = "not"; // 상태 변경
                          go1=go1-1;
                      }
                  }
              </script>
   
            </div>
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  1124 최준영
               </h1>
            </div>
         </button>
   
         <button class="button" onclick="toggleImg6()">
            <div style="float: left;">
               <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img6">
               <script>
                  var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
              
                  function toggleImg6() {
                      var imgElement = document.getElementById("img6");
              
                      // 이미지 상태에 따라 토글
                      if (img1Status === "not") {
                          imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                          img1Status = "set"; // 상태 변경
                          go1=go1+1;
                      } else {
                          imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                          img1Status = "not"; // 상태 변경
                          go1=go1-1;
                      }
                  }
              </script>
   
            </div>
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
               1201 김래현
               </h1>
            </div>
         </button>
   
         <button class="hs" onclick="toggleImg7()">
            <div style="float: left;">
               <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img7">
               <script>
                  var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
              
                  function toggleImg7() {
                      var imgElement = document.getElementById("img7");
              
                      // 이미지 상태에 따라 토글
                      if (img1Status === "not") {
                          imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                          img1Status = "set"; // 상태 변경
                          go1=go1+1;
                      } else {
                          imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                          img1Status = "not"; // 상태 변경
                          go1=go1-1;
                      }
                  }
              </script>
   
            </div>
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  1204 김창엽
               </h1>
            </div>
         </button>
   
         <button class="hs" onclick="toggleImg8()">
            <div style="float: left;">
               <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img8">
               <script>
                  var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
              
                  function toggleImg8() {
                      var imgElement = document.getElementById("img8");
              
                      // 이미지 상태에 따라 토글
                      if (img1Status === "not") {
                          imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                          img1Status = "set"; // 상태 변경
                          go1=go1+1;
                      } else {
                          imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                          img1Status = "not"; // 상태 변경
                          go1=go1-1;
                      }
                  }
              </script>
   
            </div>
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  1207 박정빈
               </h1>
            </div>
         </button>
   
         <button class="button" onclick="toggleImg9()">
            <div style="float: left;">
               <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img9">
               <script>
                  var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
              
                  function toggleImg9() {
                      var imgElement = document.getElementById("img9");
              
                      // 이미지 상태에 따라 토글
                      if (img1Status === "not") {
                          imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                          img1Status = "set"; // 상태 변경
                          go1=go1+1;
                      } else {
                          imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                          img1Status = "not"; // 상태 변경
                          go1=go1-1;
                      }
                  }
              </script>
   
            </div>
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  1210 손유민
               </h1>
            </div>
         </button>
   
         <button class="button" onclick="toggleImg10()">
            <div style="float: left;">
               <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img10">
               <script>
                  var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
              
                  function toggleImg10() {
                      var imgElement = document.getElementById("img10");
              
                      // 이미지 상태에 따라 토글
                      if (img1Status === "not") {
                          imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                          img1Status = "set"; // 상태 변경
                          go1=go1+1;
                      } else {
                          imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                          img1Status = "not"; // 상태 변경
                          go1=go1-1;
                      }
                  }
              </script>
            </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  1215 이수환
               </h1>
            </div>
         </button>
   
         <button class="button" onclick="toggleImg11()">
            <div style="float: left;">
               <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img11">
               <script>
                  var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
              
                  function toggleImg11() {
                      var imgElement = document.getElementById("img11");
              
                      // 이미지 상태에 따라 토글
                      if (img1Status === "not") {
                          imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                          img1Status = "set"; // 상태 변경
                          go1=go1+1;
                      } else {
                          imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                          img1Status = "not"; // 상태 변경
                          go1=go1-1;
                      }
                  }
              </script>
            </div>
           
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  
               </h1>
            </div>
         </button>
   
         <button class="button" onclick="toggleImg12()">
            <div style="float: left;">
               <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img12">
               <script>
                  var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
              
                  function toggleImg12() {
                      var imgElement = document.getElementById("img12");
              
                      // 이미지 상태에 따라 토글
                      if (img1Status === "not") {
                          imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                          img1Status = "set"; // 상태 변경
                          go1=go1+1;
                      } else {
                          imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                          img1Status = "not"; // 상태 변경
                          go1=go1-1;
                      }
                  }
              </script>
            </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg13()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img13">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg13() {
                   var imgElement = document.getElementById("img13");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg14()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img14">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg14() {
                   var imgElement = document.getElementById("img14");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg15()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img15">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg15() {
                   var imgElement = document.getElementById("img15");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
           
            <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg16()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img16">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg16() {
                   var imgElement = document.getElementById("img16");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg17()">
            <div style="float: left;">
               <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img17">
               <script>
                  var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
              
                  function toggleImg17() {
                      var imgElement = document.getElementById("img17");
              
                      // 이미지 상태에 따라 토글
                      if (img1Status === "not") {
                          imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                          img1Status = "set"; // 상태 변경
                          go1=go1+1;
                      } else {
                          imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                          img1Status = "not"; // 상태 변경
                          go1=go1-1;
                      }
                  }
              </script>
            </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg18()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img18">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg18() {
                   var imgElement = document.getElementById("img18");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg19()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img19">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg19() {
                   var imgElement = document.getElementById("img19");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
           
             <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  
               </h1>
            </div>
         </button>
      </div>
   
   
       <div style="width: 135px;  margin-right: 60px; height: 1150px; float: left;">
            <button class="button" onclick="toggleImg20()">
               <div style="float: left;">
               <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img20">
               <script>
                  var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
              
                  function toggleImg20() {
                      var imgElement = document.getElementById("img20");
              
                      // 이미지 상태에 따라 토글
                      if (img1Status === "not") {
                          imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                          img1Status = "set"; // 상태 변경
                          go1=go1+1;
                      } else {
                          imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                          img1Status = "not"; // 상태 변경
                          go1=go1-1;
                      }
                  }
              </script>
         </div>
         
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  1309 박현종
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg21()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img21">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg21() {
                   var imgElement = document.getElementById("img21");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
           
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  1315 이상현
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg22()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img22">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg22() {
                   var imgElement = document.getElementById("img22");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  1317 이승민
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg23()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img23">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg23() {
                   var imgElement = document.getElementById("img23");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  1318 이승헌
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg24()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img24">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg24() {
                   var imgElement = document.getElementById("img24");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  1328 허승건
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg25()">
   
      <div style="float: left;">
         <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img25">
         <script>
            var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
        
            function toggleImg25() {
                var imgElement = document.getElementById("img25");
        
                // 이미지 상태에 따라 토글
                if (img1Status === "not") {
                    imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                    img1Status = "set"; // 상태 변경
                } else {
                    imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                    img1Status = "not"; // 상태 변경
                }
            }
        </script>
      </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  1401 권오형
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg26()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img26">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg26() {
                   var imgElement = document.getElementById("img26");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  1408 박시민
               </h1>
            </div>
         </button>
      
      <button class="hs" onclick="toggleImg27()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img27">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg27() {
                   var imgElement = document.getElementById("img27");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
   
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  1414 손서준
               </h1>
            </div>
         </button>
      
      <button class="hs" onclick="toggleImg28()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img28">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg28() {
                   var imgElement = document.getElementById("img28");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  1421 이재현
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg29()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img29">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg29() {
                   var imgElement = document.getElementById("img29");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  1425 최형준
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg30()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img30">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg30() {
                   var imgElement = document.getElementById("img30");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  1501 강성주
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg31()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img31">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg31() {
                   var imgElement = document.getElementById("img31");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
         <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
          </div>
      </button>
      
      <button class="button" onclick="toggleImg32()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img32">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg32() {
                   var imgElement = document.getElementById("img32");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
            
            <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg33()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img33">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg33() {
                   var imgElement = document.getElementById("img33");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg34()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img34">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg34() {
                   var imgElement = document.getElementById("img34");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg35()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img35">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg1() {
                   var imgElement = document.getElementById("img1");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg36()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img36">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg1() {
                   var imgElement = document.getElementById("img1");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
           
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg37()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img37">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg37() {
                   var imgElement = document.getElementById("img37");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg38()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img38">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg38() {
                   var imgElement = document.getElementById("img38");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
            
            <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
            </div>
         </button>
   
      </div>
   
       <div style="width: 135px;  margin-right: 60px; height: 1150px; float: left;">
       <button class="button" onclick="toggleImg39()">
            <div style="float: left;">
               <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img39">
               <script>
                  var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
              
                  function toggleImg39() {
                      var imgElement = document.getElementById("img39");
              
                      // 이미지 상태에 따라 토글
                      if (img1Status === "not") {
                          imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                          img1Status = "set"; // 상태 변경
                          go1=go1+1;
                      } else {
                          imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                          img1Status = "not"; // 상태 변경
                          go1=go1-1;
                      }
                  }
              </script>
            </div>
            
            <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  1506 김채준
               </h1>
            </div>
       </button>
      
       <button class="button" onclick="toggleImg40()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img40">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg40() {
                   var imgElement = document.getElementById("img40");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
           
         <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  1513 이윤호
               </h1>
         </div>
       </button>
      
      <button class="hs" onclick="toggleImg41()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img41">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg41() {
                   var imgElement = document.getElementById("img41");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  1520 조민현
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg42()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img42">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg42() {
                   var imgElement = document.getElementById("img42");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
           
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                 1524 최민기
               </h1>
            </div>
         </button>
      
      <button class="hs" onclick="toggleImg43()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img43">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg43() {
                   var imgElement = document.getElementById("img43");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  1527 황정찬
               </h1>
            </div>
         </button>
      
      <button class="hs" onclick="toggleImg44()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img44">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg44() {
                   var imgElement = document.getElementById("img44");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  1604 권예준
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg45()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img45">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg45() {
                   var imgElement = document.getElementById("img45");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  1605 김건호
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg46()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img46">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg46() {
                   var imgElement = document.getElementById("img46");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  1606 김민재
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg47()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img47">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg47() {
                   var imgElement = document.getElementById("img47");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
           
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  1608 김은찬
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg48()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img48">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg48() {
                   var imgElement = document.getElementById("img48");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  1613 나도엽
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg49()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img49">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg49() {
                   var imgElement = document.getElementById("img49");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  1614 문해찬
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg50()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img50">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg50() {
                   var imgElement = document.getElementById("img50");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg51()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img51">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg51() {
                   var imgElement = document.getElementById("img51");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
           
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg52()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img52">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleIm52() {
                   var imgElement = document.getElementById("img52");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg53()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img53">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg53() {
                   var imgElement = document.getElementById("img53");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg54()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img54">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg54() {
                   var imgElement = document.getElementById("img54");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
           
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg55()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img55">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg55() {
                   var imgElement = document.getElementById("img55");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg56()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img56">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg56() {
                   var imgElement = document.getElementById("img56");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg57()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img57">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg57() {
                   var imgElement = document.getElementById("img57");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
           
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
            </div>
         </button>
   
      </div>
   
       <div style="width: 135px;  margin-right: 60px; height: 1150px; float: left;">
         <button class="button" onclick="toggleImg58()">
            <div style="float: left;">
               <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img58">
               <script>
                  var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
              
                  function toggleImg58() {
                      var imgElement = document.getElementById("img58");
              
                      // 이미지 상태에 따라 토글
                      if (img1Status === "not") {
                          imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                          img1Status = "set"; // 상태 변경
                          go1=go1+1;
                      } else {
                          imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                          img1Status = "not"; // 상태 변경
                          go1=go1-1;
                      }
                  }
              </script>
            </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  1624 정서경
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg59()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img59">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg59() {
                   var imgElement = document.getElementById("img59");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  1626 최서인
               </h1>
            </div>
         </button>
      
      <button class="hs" onclick="toggleImg60()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img60">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg60() {
                   var imgElement = document.getElementById("img60");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
           
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  1705 김동인
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg61()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img61">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg61() {
                   var imgElement = document.getElementById("img61");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
   
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  1709 김시원
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg62()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img62">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg62() {
                   var imgElement = document.getElementById("img62");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
           
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  1717 배현수
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg63()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img63">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg63() {
                   var imgElement = document.getElementById("img63");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
          
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  1720 이인욱
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg64()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img64">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg64() {
                   var imgElement = document.getElementById("img64");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
           
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  1727 홍지성
               </h1>
            </div>
         </button>
      
      <button class="hs" onclick="toggleImg65()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img65">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg65() {
                   var imgElement = document.getElementById("img65");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
           
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  1802 김세동
               </h1>
            </div>
         </button>
      
         <button class="button" onclick="toggleImg66()">
            <div style="float: left;">
               <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img66">
               <script>
                  var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
              
                  function toggleImg66() {
                      var imgElement = document.getElementById("img66");
              
                      // 이미지 상태에 따라 토글
                      if (img1Status === "not") {
                          imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                          img1Status = "set"; // 상태 변경
                          go1=go1+1;
                      } else {
                          imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                          img1Status = "not"; // 상태 변경
                          go1=go1-1;
                      }
                  }
              </script>
            </div>
               
                        <div style="float: right; height: 30px;">
                  <h1 style="font-size: 15px; margin: 0px;">
                     1808 박건희
                  </h1>
               </div>
            </button>
      
         <button class="button" onclick="toggleImg67()">
            <div style="float: left;">
               <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img67">
               <script>
                  var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
              
                  function toggleImg67() {
                      var imgElement = document.getElementById("img67");
              
                      // 이미지 상태에 따라 토글
                      if (img1Status === "not") {
                          imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                          img1Status = "set"; // 상태 변경
                          go1=go1+1;
                      } else {
                          imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                          img1Status = "not"; // 상태 변경
                          go1=go1-1;
                      }
                  }
              </script>
            </div>
               
                        <div style="float: right; height: 30px;">
                  <h1 style="font-size: 15px; margin: 0px;">
                     1811 손승열
                  </h1>
               </div>
            </button>
      
      <button class="button" onclick="toggleImg68()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img68">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg68() {
                   var imgElement = document.getElementById("img68");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  1817 이채환
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg69()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img69">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg69() {
                   var imgElement = document.getElementById("img69");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
          
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  1826 최윤성
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg70()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img70">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg70() {
                   var imgElement = document.getElementById("img70");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
          
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg71()">
         <div style="float: left;">
   
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img71">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg71() {
                   var imgElement = document.getElementById("img71");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg72()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img72">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg72() {
                   var imgElement = document.getElementById("img72");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg73()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img73">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg73() {
                   var imgElement = document.getElementById("img73");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg74()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img74">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg74() {
                   var imgElement = document.getElementById("img74");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
           
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg75()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img75">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg75() {
                   var imgElement = document.getElementById("img75");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
           
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg76()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img76">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg76() {
                   var imgElement = document.getElementById("img76");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
            </div>
         </button>
      </div>
   
       <div style="width: 135px;  margin-right: 60px; height: 1150px; float: left;">
         <button class="button" onclick="toggleImg77()">
            <div style="float: left;">
               <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img77">
               <script>
                  var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
              
                  function toggleImg77() {
                      var imgElement = document.getElementById("img77");
              
                      // 이미지 상태에 따라 토글
                      if (img1Status === "not") {
                          imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                          img1Status = "set"; // 상태 변경
                          go1=go1+1;
                      } else {
                          imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                          img1Status = "not"; // 상태 변경
                          go1=go1-1;
                      }
                  }
              </script>
            </div>
          
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  2109 신서형
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg78()">
         <div style="float: left;"> 
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img78">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg78() {
                   var imgElement = document.getElementById("img78");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
   
         </div>
           
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  2111 엄채호
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg79()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img79">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg79() {
                   var imgElement = document.getElementById("img79");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
           
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  2113 윤주승
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg80()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img80">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg80() {
                   var imgElement = document.getElementById("img80");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
           
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  2116 이다온
               </h1>
            </div>
         </button>
      
      <button class="hs2" onclick="toggleImg81()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img81">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg81() {
                   var imgElement = document.getElementById("img81");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  2123 현재민
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg82()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img82">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg82() {
                   var imgElement = document.getElementById("img82");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  2208 서진수
               </h1>
            </div>
         </button>
      
      <button class="hs2" onclick="toggleImg83()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img83">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg83() {
                   var imgElement = document.getElementById("img83");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
           
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  2212 이가빈
               </h1>
            </div>
         </button>
      
         <button class="button" onclick="toggleImg84()">
            <div style="float: left;">
               <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img84">
               <script>
                  var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
              
                  function toggleImg84() {
                      var imgElement = document.getElementById("img84");
              
                      // 이미지 상태에 따라 토글
                      if (img1Status === "not") {
                          imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                          img1Status = "set"; // 상태 변경
                          go1=go1+1;
                      } else {
                          imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                          img1Status = "not"; // 상태 변경
                          go1=go1-1;
                      }
                  }
              </script>
            </div>
               
                        <div style="float: right; height: 30px;">
                  <h1 style="font-size: 15px; margin: 0px;">
                     2214 이상민
                  </h1>
               </div>
            </button>
      
      <button class="button" onclick="toggleImg85()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img85">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg85() {
                   var imgElement = document.getElementById("img85");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  2216 이재진
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg86()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img86">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg86() {
                   var imgElement = document.getElementById("img86");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
           
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  2218 정주원
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg87()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img87">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg87() {
                   var imgElement = document.getElementById("img87");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg88()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img88">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg88() {
                   var imgElement = document.getElementById("img88");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
           
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg89()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img89">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg89() {
                   var imgElement = document.getElementById("img89");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
          
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg90()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img90">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg90() {
                   var imgElement = document.getElementById("img90");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg91()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img91">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg91() {
                   var imgElement = document.getElementById("img91");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg92()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img92">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg92() {
                   var imgElement = document.getElementById("img92");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg93()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img93">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg93() {
                   var imgElement = document.getElementById("img93");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
           
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg94()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img94">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg94() {
                   var imgElement = document.getElementById("img94");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
           
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg95()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img95">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg95() {
                   var imgElement = document.getElementById("img95");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
           
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
            </div>
         </button>
      </div>
   
       <div style="width: 135px;  margin-right: 60px; height: 1150px; float: left;">
            <button class="button" onclick="toggleImg96()">
               <div style="float: left;">
                  <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img96">
                  <script>
                     var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
                 
                     function toggleImg96() {
                         var imgElement = document.getElementById("img96");
                 
                         // 이미지 상태에 따라 토글
                         if (img1Status === "not") {
                             imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                             img1Status = "set"; // 상태 변경
                         } else {
                             imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                             img1Status = "not"; // 상태 변경
                         }
                     }
                 </script>
               </div>
         
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  2311 송지효
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg97()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img97">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg97() {
                   var imgElement = document.getElementById("img97");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
         
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  2313 오윤우
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg98()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img98">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg98() {
                   var imgElement = document.getElementById("img98");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
           
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  2317 이예찬
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg99()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img99">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg99() {
                   var imgElement = document.getElementById("img99");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
          
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  2318 이하윤
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg100()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img100">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg100() {
                   var imgElement = document.getElementById("img100");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
           
          <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  2407 김찬우
               </h1>
            </div>
         </button>
      
      <button class="hs2" onclick="toggleImg101()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img101">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg101() {
                   var imgElement = document.getElementById("img101");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  2417 이태현
               </h1>
            </div>
         </button>
      
      <button class="hs2" onclick="toggleImg102()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img102">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg102() {
                   var imgElement = document.getElementById("img102");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
           
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  2415 임태영
               </h1>
            </div>
         </button>
      
      <button class="hs2" onclick="toggleImg103()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img103">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg103() {
                   var imgElement = document.getElementById("img103");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
           
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  2419 채유건
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg104()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img104">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg104() {
                   var imgElement = document.getElementById("img104");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
           
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  2421 최종훈
               </h1>
            </div>
         </button>
      
      <button class="hs2" onclick="toggleImg105()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img105">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg105() {
                   var imgElement = document.getElementById("img105");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
           
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  2422 최준현
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg106()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img106">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg106() {
                   var imgElement = document.getElementById("img106");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg107()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img107">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg107() {
                   var imgElement = document.getElementById("img107");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg108()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img107">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg108() {
                   var imgElement = document.getElementById("img108");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
           
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg109()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img109">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg109() {
                   var imgElement = document.getElementById("img109");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
           
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg110()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img110">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg110() {
                   var imgElement = document.getElementById("img110");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
           
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg111()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img111">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg111() {
                   var imgElement = document.getElementById("img111");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
           
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg112()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img112">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg112() {
                   var imgElement = document.getElementById("img112");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
           
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg113()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img113">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg113() {
                   var imgElement = document.getElementById("img113");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
           
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg114()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img114">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg114() {
                   var imgElement = document.getElementById("img114");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
           
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
            </div>
         </button>
      </div>
   
       <div style="width: 135px;  margin-right: 60px; height: 1150px; float: left;">
            <button class="hs2" onclick="toggleImg115()">
               <div style="float: left;">
               <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img115">
               <script>
                  var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
              
                  function toggleImg115() {
                      var imgElement = document.getElementById("img115");
              
                      // 이미지 상태에 따라 토글
                      if (img1Status === "not") {
                          imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                          img1Status = "set"; // 상태 변경
                          go1=go1+1;
                      } else {
                          imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                          img1Status = "not"; // 상태 변경
                          go1=go1-1;
                      }
                  }
              </script>
               </div>
        
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  2507 김한음
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg116()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img116">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg116() {
                   var imgElement = document.getElementById("img116");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  2510 박상화
               </h1>
            </div>
         </button>
      
      <button class="hs2"onclick="toggleImg117()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img117">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg117() {
                   var imgElement = document.getElementById("img117");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  2514 이호준
               </h1>
            </div>
         </button>
      
      <button class="hs2"onclick="toggleImg118()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img118">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg118() {
                   var imgElement = document.getElementById("img118");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
           
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  2515 임하준
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg119()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img119">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg119() {
                   var imgElement = document.getElementById("img119");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
          
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  2516 장민준
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg120()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img120">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg120() {
                   var imgElement = document.getElementById("img120");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  2610 박주원
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg121()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img121">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg121() {
                   var imgElement = document.getElementById("img121");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  2613 배지환
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg122()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img122">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg122() {
                   var imgElement = document.getElementById("img122");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  2616 송세영
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg123()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img123">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg123() {
                   var imgElement = document.getElementById("img123");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
          
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  2621 정하준
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg124()">
         <div style="float: left;">
         
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img124">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg124() {
                   var imgElement = document.getElementById("img124");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  2623 형성진
               </h1>
            </div>
         </button>
      
      <button class="hs2"onclick="toggleImg125()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img125">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg125() {
                   var imgElement = document.getElementById("img125");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
           
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  2624 황민준
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg126()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img126">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg126() {
                   var imgElement = document.getElementById("img126");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
           
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg127()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img127">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg127() {
                   var imgElement = document.getElementById("img127");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
           
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg128()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img128">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg128() {
                   var imgElement = document.getElementById("img128");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
          
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg129()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img129">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg129() {
                   var imgElement = document.getElementById("img129");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg130()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img130">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg130() {
                   var imgElement = document.getElementById("img130");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
           
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg131()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img131">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg131() {
                   var imgElement = document.getElementById("img131");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg132()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img132">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg132() {
                   var imgElement = document.getElementById("img132");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
           
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg133()">
         <div style="float: left;">
             <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img133">
             <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg133() {
                   var imgElement = document.getElementById("img133");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
   
         </div>
           
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
            </div>
         </button>
      </div>
   
      <div style="width: 135px; float: left;">
         <button class="hs2" onclick="toggleImg134()">
            <div style="float: left;">
               <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img134">
               <script>
                  var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
              
                  function toggleImg134() {
                      var imgElement = document.getElementById("img134");
              
                      // 이미지 상태에 따라 토글
                      if (img1Status === "not") {
                          imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                          img1Status = "set"; // 상태 변경
                          go1=go1+1;
                      } else {
                          imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                          img1Status = "not"; // 상태 변경
                          go1=go1-1;
                      }
                  }
              </script>
            </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  2705 김일훈
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg135()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img135">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg135() {
                   var imgElement = document.getElementById("img135");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
           
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  2713 안상민
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg136()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img136">
            
          <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg136() {
                   var imgElement = document.getElementById("img136");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
         
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  2721 조민관
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg137()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img137">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg137() {
                   var imgElement = document.getElementById("img137");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  2722 조현승
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg138()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img138">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg138() {
                   var imgElement = document.getElementById("img138");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
           
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  2723 허재영
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg139()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img139">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg139() {
                   var imgElement = document.getElementById("img139");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
           
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  2804 박민우
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg140()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img140">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg140() {
                   var imgElement = document.getElementById("img140");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  2810 이원겸
               </h1>
            </div>
         </button>
   
         <button class="button" onclick="toggleImg141()">
            <div style="float: left;">
               <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img141">
               <script>
                  var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
              
                  function toggleImg141() {
                      var imgElement = document.getElementById("img141");
              
                      // 이미지 상태에 따라 토글
                      if (img1Status === "not") {
                          imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                          img1Status = "set"; // 상태 변경
                          go1=go1+1;
                      } else {
                          imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                          img1Status = "not"; // 상태 변경
                          go1=go1-1;
                      }
                  }
              </script>
            </div>
               
                        <div style="float: right; height: 30px;">
                  <h1 style="font-size: 15px; margin: 0px;">
                     2813 정무창
                  </h1>
               </div>
            </button>
      
      <button class="hs2" onclick="toggleImg142()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img142">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg142() {
                   var imgElement = document.getElementById("img142");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                  2816 조승현
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg143()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img143">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg143() {
                   var imgElement = document.getElementById("img143");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg144()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img144">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg144() {
                   var imgElement = document.getElementById("img144");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg145()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img145">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg145() {
                   var imgElement = document.getElementById("img145");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
           
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg146()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img146">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg146() {
                   var imgElement = document.getElementById("img146");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
           
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg147()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img147">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg147() {
                   var imgElement = document.getElementById("img147");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg148()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img148">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg148() {
                   var imgElement = document.getElementById("img148");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
           
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg149()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img149">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg149() {
                   var imgElement = document.getElementById("img149");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
            
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg150()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img150">
     
          <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg150() {
                   var imgElement = document.getElementById("img150");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
           
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg151()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img151">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg151() {
                   var imgElement = document.getElementById("img151");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
          
                     <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
            </div>
         </button>
      
      <button class="button" onclick="toggleImg152()">
         <div style="float: left;">
            <img src="https://i.ibb.co/FJfC1tK/not.png" style="height: 25px; width: 25px;" id="img152">
            <script>
               var img1Status = "not"; // 초기 이미지 상태를 저장하는 변수
           
               function toggleImg152() {
                   var imgElement = document.getElementById("img152");
           
                   // 이미지 상태에 따라 토글
                   if (img1Status === "not") {
                       imgElement.src = "https://i.ibb.co/4Rrvrz0/set.png";
                       img1Status = "set"; // 상태 변경
                   } else {
                       imgElement.src = "https://i.ibb.co/FJfC1tK/not.png";
                       img1Status = "not"; // 상태 변경
                   }
               }
           </script>
         </div>
          
         <div style="float: right; height: 30px;">
               <h1 style="font-size: 15px; margin: 0px;">
                   
               </h1>
         </div>
         </button>
      </div>

   </div>

 </div>

      

</body>

</html>
