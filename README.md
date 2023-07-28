[사이트바로가기](https://nam-seungjin.github.io/report08)

# workprocess

# TOURIST
## 목적
여러 여행사 사이트를 보면서 여행지 사진이 자동으로 넘겨지지 않은 문제점을 보았기 때문에 이것을 개선해 보고자 자동 슬라이드가 적용되는 사이트를 제작해 보았습니다.
그리고 사진을 클릭할 시 더 크게 보이는 것이 관심을 끌 것이라는 저의 생각에 클릭 이벤트도 적용되게 제작해 보았습니다   
### 개선
이런 슬라이드를 개선하고자 사진이 자동으로 넘겨지는 것을 적용하기 위한 코드와
사진 클릭 시 컬러로 보이는 것하고 크게 보이는 코드를 입력하였습니다.
#### 기술
// 자동 슬라이드 이벤트



let cngSlider = setInterval(mySlider,4000);

            // 슬라이더 멈춤 이벤트
            $('.stop').click(function(){
                clearInterval(cngSlider);
                $(this).css('display','none');
                $('.start').css('display','block');
            })
            // 슬라이더 재실행 이벤트
            $('.start').click(function(){
                cngSlider = setInterval(mySlider,4000);
                $(this).css('display','none');
                $('.stop').css('display','block');
            })




pager 클릭 하지 않은 경우엔



#travel .img-box{
filter:gratscale(1);
}



pager 클릭한 경우엔



#travel .img-box:hover{
filter:gratscale(0);
}



이렇게 코드를 입력해 클릭하지 않을 때는 흑백 클릭 시 컬러로 보이게 코드를 입력했습니다.



//pager 클릭 이벤트



            btnNums.click(function(){
               idx = $(this).index() - 1;
               clearInterval(cngSlider);
               mySlider();
               cngSlider = setInterval(mySlider,4000);
            })

            $('#travel a').click(function(){
                return false;
            })
            
            $('#travel article').click(function(){
                console.log($(this));
            })

            let docHeight;
            function fnDocHeight(){
                docHeight = $(document).height();
                $('.pop-box').css('height',`${docHeight}px`);
                
            }
            fnDocHeight();
 
            $('#travel article').click(function(){
                $(this).children('.pop-box').toggle(0);
            })

            ##### 작업기간
            기간은 1주일 소요 됐습니다.

