


- [x] hotfix/seasonpass_lv_reward_bug_fix ✅ 2023-09-18 
       시즌패스 레벨보상 받고 탭 이동후 복귀시 갱신 안되어있는 현상 수정
- [x] origin/hotfix/multi_schedule_chapteropen_bug_fix ✅ 2023-09-18
      멀티스케쥴 챕터오픈 연출이 반복적으로 나오는 현상 수정
- [x] origin/hotfix/coop_schedule_my_ranking_ui_bug_fix ✅ 2023-09-18
      협동전 내 랭킹 100위 넘어가면 ui가 0으로 나오는 현상 수정
- [x] origin/hotfix/buildqa_patternoid_mission_event_bug_fix ✅ 2023-09-18
      스케쥴 별3개 달성 클리어 조건 시 상태값 잘못 설정되는 이슈 수정
- [x] hotfix/coop_schedule_my_ranking_ui_bug_fix ✅ 2023-09-18
      내랭킹이 100위 넘어가면 퍼센트로 출력(협동전팝업내에서만)
- [x] origin/hotfix/attend_max_check ✅ 2023-09-18
      출석부 보상받을때 (음반보상이 아니여도) 음반MAX를 무조건 체크하는 이슈
- [x] origin/hotfix/tutorial_3_savepoint ✅ 2023-09-18
      튜토리얼 3번(음반제작소 튜토리얼) 저장시점 수정
- [x] --- ✅ 2023-09-18
      상품 버튼의 레드닷
- [x] hotfix/guide_weblink ✅ 2023-09-18
      hotfix/guide_weblink
- [x] origin/hotfix/shortcut_exception ✅ 2023-09-18
      fix: GotoShortcut Null exception
- [x] hotfix/buildqa_patternoid_bpworld_chat_button_disable_bug_fix ✅ 2023-09-20
      블핑월드 메인이벤트 팝업 내 특정 팝업 뜰 시 채팅 버튼 사라지는 버그 수정
- [x] hotfix/buildqa_patternoid_maineventpopup_null_exception ✅ 2023-09-20
      null Exception 수정
- [x] hotfix/buildqa_patternoid_mission_excute_event_bug_challenge_bug_fix ✅ 2023-09-20
      미션 수행 이벤트 미션 리스트 상태 버그 수정
- [x] hotfix/advertise_colltime_zero_check ✅ 2023-09-20
      메일함 광고 쿨타임 수정
- [x] hotfix/coop_story_save ✅ 2023-09-20
      협동전 스토리텔링노출 저장여부 키값에 cms_event_idx 추가.
- [x] hotfix/special_schedule_member_info_0921 ✅ 2023-09-21
      개인스케줄 퍼즐 시작연출 멤버정보 지수만 나오는 UI 수정.
- [x] hotfix/webview_to_event ✅ 2023-09-21
      웹뷰 딥링크 추가 작업 (상점,뽑기,성장반복이벤트,미션수행이벤트)





#### qa빌드 체크

 - 데이터 체크
 - 서버패치 체크
 - 번들 체크
 - 패치 용량 체크 - 1.03.082 보다 177mb 증가


#### 웹뷰 딥링크

상점 
target = shop
id 1개 추가
callback://navigation?target=shop&id=3410480001

뽑기 
target = gacha
id 1개 추가
callback://navigation?target=gacha&id=350200001


성장반복이벤트
target 추가 growth
id 3개 추가
callback://navigation?target=growth&id=336000101
callback://navigation?target=growth&id=336000201
callback://navigation?target=growth&id=336000301

미션수행이벤트
target 추가 mission
id 2개 추가
callback://navigation?target=mission&id=3341001
callback://navigation?target=mission&id=3341002