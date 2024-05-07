
InitializeAsObservable() 함수에서 UserDataService.ItemlistInfo() 호출시작

### API flow

- UserDataService.ItemlistInfo()
- CDataSettingController.SetServerData() - LobbyTop
	- Landing 
	- Title
- LobbyTop 응답에서 튜토리얼체크



- TitleCanvasManager.OnClickStartBtn() 에서
	- CPlayer.Instance.Lading.Value - 랜딩 플레이 체크 여부. 
		- true - 랜딩 플레이완료
		- false - 랜딩씬으로 씬이동