# 컨피그 체크 사항
  ## AOS, iOS 공통
 -   #### CMS config 속성
      - **공통속성** 
  
        1.  <span style="background-color:#FFE6E6"> **game_policy_url** </span> - 점검공지 URL ( https://www.takeonecompany.com/games/bptg/board.html?board=notice&content=MAINTENANCE0823 )
        2.  private_url - https://www.takeonecompany.com
        3.  protect_url - https://www.takeonecompany.com
        4.  terms_url - https://www.takeonecompany.com
        5.  market_url 
            -  https://play.google.com/store/apps/details?id=com.takeonecompany.bptg1
            -  https://apps.apple.com/kr/app/blackpink-the-game/id6444351044
        6.  can_select_game_setting - <span style="background-color:#FFE6E6"> **F ( live, review 는 무조건 F )** </span>   
   
      
      ---

      - **개별속성**
    
        1.  <span style="background-color:#FFE6E6"> **version** </span> - 게임버전
        2.  name - config 파일 이름
        3.  priority_of_version - version이 같을경우 우선순위.
        4.  cdn_address - CDN 주소
        5.  game_server_address - 게임서버 주소
        6.  <span style="background-color:#FFE6E6"> **session_server_address** - **Live 일경우에만 LIVE** ( 그외 모든경우 CPDEV. 마켓검수도 CPDEV )
        7.  chat_server_address - 채팅서버 주소
        8.  <span style="background-color:#FFE6E6"> **resource_version** 
            - <span style="background-color:#FFE6E6"> **game_data**  - GD 버전
            - <span style="background-color:#FFE6E6"> **resources**  - 어셋번들 리소스 버전
            ```
            빌드qa 완료후  릴리즈서버에서 gd생성, 어셋번들생성해서 
            발생한 gd, resources 버전 입력
            ```


        9.  region  
            - <span style="background-color:#FFE6E6"> **is_region_use**  - 리전 사용여부 ( LIVE 에서만 T, 마켓검수도 리전 사용안함 )
            - asia_1 
              - cdn_address - 리전별 cdn 주소
              - game_server_address - 리전별 게임서버 주소
              - chat_server_address - 리전별 채팅서버 주소
            - asia_2 
              - cdn_address - 리전별 cdn 주소
              - game_server_address - 리전별 게임서버 주소
              - chat_server_address - 리전별 채팅서버 주소 
            - us 
              - cdn_address - 리전별 cdn 주소
              - game_server_address - 리전별 게임서버 주소
              - chat_server_address - 리전별 채팅서버 주소
            - eu 
              - cdn_address - 리전별 cdn 주소
              - game_server_address - 리전별 게임서버 주소
              - chat_server_address - 리전별 채팅서버 주소

              
        10. <span style="background-color:#FFE6E6"> **maintenance**  
            - <span style="background-color:#FFE6E6">**is_maintenance** - 점검 세팅 여부 ( T:점검on, F:점검off )
            - <span style="background-color:#FFE6E6">**minimum_version** - 해당 버전 이하는 점검이 걸린다. ( 0.00.000 )
            - <span style="background-color:#FFE6E6">**end_time** - 점검 종료시간 ( 2023/08/01 17:30 )
            - <span style="background-color:#FFE6E6">**messages** - 점검의 성격에 맞는 메세지를 선택한다. ( 정기점검, 긴급점검, 업데이트점검, 신규이벤트점검, 연장점검 )
            - <span style="background-color:#FFE6E6"> **allow_list** - **화이트리스트.** 점검중 입장해야하는 pid를 세팅한다. 
                ```
                https://docs.google.com/spreadsheets/d/1OrZGxTGO5r684qvSvYvYvubM0GBWsJx6ruflZ-MT9vw/edit#gid=0
                입력된 화이트리스트를 복사해서 넣는다. 
                
                ```
        11. <span style="background-color:#FFE6E6">**update**  
            - <span style="background-color:#FFE6E6">**minimum_version** - 해방버전 이하는 강제 업데이트 하도록 한다. ( 0.00.000 )
        12. etc
            - is_check_downloaded_resource_file_hash - F ( 리소스업데이트 체크할때 해시체크여부, 현재는 사용하지 않는다. 무조건 해시체크를 안하고 있다 )
            - <span style="background-color:#FFE6E6">**is_otp** - F ( OTP 노출 여부 )
            - tcp_server_db_num - 0 
            - <span style="background-color:#FFE6E6">**ad_flag** - 테스트광고 여부. LIVE에서만 T 사용. ( T:라이브광고, F:테스트광고 )
            - pre_download - F
            - open_datetime - 2023/05/18 11:00 ( 런칭때 사용 )
            - test_num_1 - 개발 테스트용
            - test_num_2 - 개발 테스트용
            - test_num_3 - 개발 테스트용

___
___
___
___
      
---


  # 검수빌드 업로드 Review App bundle Upload 

  -  **안드로이드 검수빌드는 내부테스트( internal testing ) 메뉴에서 업로드 해야한다.**
  -  **애플 검수 빌드는 동일하게 테스트플라이트에 업로드 한다.**







---

 ## 컨피그 업로드 하기

```
172.27.14.50 원격접속
id : take0ne
pw : take1234

```

**1. S3 Browser 프로그램 실행**
1. Accout > BPTG_LIVE (AWS)
2. Accout > ncloud

### - **반드시 AWS/NCloud 양쪽 CDN 모두 업로드 해야함.**

```
Live에서 ncloud 사용하고 있지만 속도의 문제때문에 AWS로 바로 전향할수 있으니 gd/res 둘다 올려야 함
```

 #### GD / Resources 업로드
- nas1에서 업로드할 파일/폴더를 찾아서 경로에 맞게 드래그앤드랍 함
- 복사된 파일/폴더 선택함.
- 파일/폴더 선택된 상태에서 하단 메뉴 탭에서 "Permissions" 선택
- 맨아래 "Make Public" 선택 하면 설정 끝
    - ( gd/resources 는 항상 새 파일이므로 퍼지 할 필요 없음 )

 #### Config 업로드
- config 폴더 통째로 드래그앤드랍 함.
  - ( config 파일은 퍼지가 필요함 )
- config/ 폴더에서 오른쪽 마우스 메뉴 클릭
- CloudFront > Invlidate selected files 클릭 ( 이게 퍼지메뉴 )
- 맨아래 "Make Public" 선택 하면 설정 끝

  


---

       
 ## 컨피그 업로드 후 체크 사항



  1. 브라우저에서 컨피그 확인
    * [cdn_address]/config/[os]/release/config.json 으로 브라우저에서 확인. 
    * ex) https://cdnaddress/config/android/release/config.json

###검수빌드 
      https://d3t8h2nevf8jwd.cloudfront.net/config/android/release/config.json
      https://d3t8h2nevf8jwd.cloudfront.net/config/ios/release/config.json

  



---


## 릴리즈 uuid override 하는법 
  - gateservice.cs 126 라인 develop 제한 해제하기.
  - pid : 7S8KYVK1-Z6M85L71Z9VPIN8NCRP1EM5
  - uuid : 1C8F29ED-2711-45CF-A0BF-A9F8D0D97E08
  - 유니티 에디터 메뉴 Takeone - platform - api - platfomtestwindow


---


# ---------- 검수빌드 세팅할때 주의 사항 ------------------


 ### 1. 현재 라이브컨피그에 버전이 빌드 버전과 맞는지 체크한다. ( 권장업데이트로 버전이 다를수 있다. ) 
 ### 2. 라이브컨피그 버전이 다르거나 낮을경우 현재 빌드버전과 맞춘다. ( 권장업데이트가 있을경우 미니멈버전을 맞춰준다 )
 ### 3. 마켓검수용 컨피그에 검수빌드버전과 gd, resources 를 세팅한다. 
 ### 4. 컨피그 업로드를 진행한다.





# ---------- 라이브 업데이트 점검 순서 ------------------



 ### 1. 현재 빌드버전 그상태에서 클라이언트 컨피그 점검 세팅. 
 ### 2. 검수빌드 컨피그 버전 0.00.001 로 변경. 
 ### 3. 마켓에 빌드 배포.
 ### 4. 화이트리스트 세팅. ( 구글독스의 화이트리스트 갱신 체크. 생성된 화이트리스트를 삭제하고 다시 생성하는게 좋음. )
 ### 5. gd, resources 버전 세팅.
 ### 6. 점검중 할일 .... tgp작업. server patch, event setting, shop product setting.....
 ### 7. 마켓에서 빌드 노출되면 최신버전으로 버전세팅. 화이트리스트 제거