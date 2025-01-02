

- <span style="background:#affad1">1231 CDN Patch 리소스 관리.</span>
	- 카드 등의 리소스를 업로드 하도록 브랜치 생성후 제공. ( update_resources/card_20250107_cdnpatch )
- 리소스 브랜치를 design 브랜치에 머지 (기획팀 요청)
- design 브랜치에서 기획팀이 체크
- design 브랜치에서 체크 완료후 patch_qa 브랜치로 머지.
- patch_qa 브랜치에서 어셋번들 생성. 
- 생성된 어셋번들을 1.00.252 빌드에서 확인 가능하도록 config 세팅
	- 1231 CDN Patch 는  1.00.252(build_qa) 빌드가 라이브 빌드와 동일하므로 build_qa의 config에  config 추가로 생성해서 적용. 
	- 젠킨스로 번들 생성시에 브랜치는 patch_qa로 하고 업로드폴더는 build_qa로 세팅후 젠킨스 빌드. or patch_qa에서 생성된 번들은 build_qa폴더에 옮겨야 함. 
- QA팀에 patch_qa 적용했다고 전달. 


![[Pasted image 20241219152330.png]]




