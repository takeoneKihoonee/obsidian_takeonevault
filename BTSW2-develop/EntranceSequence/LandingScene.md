
- LandingScene
	- Utility.FallbackFont -> FallbackFontLoaderController


- FallbackFontLoaderController
	- FallbackFontLoaderController.prefab


- LandingCanvasManager
	- addchild -> PageLanding


- PageLanding
	- page_landing.prefab


- OnClick_BtnNickNameConfirm()
	- APIHelper.Auth.SignIn() - nickname
	- APIHelper.UserDataService.MemberSelectInfo - 멤버선택 
	- 남은 랜딩타임라인 landing download 시도를 InitializeAsObservable 함수호출로 함. ;;;;;
	- InitializeAsObservable()
		- APIHelper.UserDataService.ItemlistInfo()
		- CDataSettingController.Instance.SetServerData() - lobbytop
		- APIHelper.UserDataService.ADList() 
		- CUnlockSystemManager.Instance.SetData() - 언락세팅
		- DownloadFile(key) -  랜딩 추가 다운로드