**File:** `Flaunch.szs`  
**Main `bflyt` file:** [`FlcCntMain.bflyt`](FlcCntMain.bflyt.md)

---

## Layout Files in `Flaunch.szs`

<!-- prettier-ignore -->
!!! Info
    These aren't all files, because either the function is unknown or the component is unimportant.

| Filename                     | Hypothetical full name            | Function                                                                           |
| ---------------------------- | --------------------------------- | ---------------------------------------------------------------------------------- |
| AreaNml.bflyt		       | AreaNormal				 | Defines scroll/touch/cursor area							      	  |
| AreaNmlL.bflyt		       | AreaNormalLarge			 | Scroll/touch/cursor Larger area									  |
| AreaNmlLGrp.bflyt	       | AreaNormalLargeGroup		       | Scroll/Touch/Cursor group windows							        |
| AreaNmlNav.bflyt	       | AreaNormalNavigation		       | Scroll/Touch/Cursor Navigation area (side of add/create group)		      	  |	
| AreaNmlNavMain.bflyt	       | AreaNormalNavigationMain(window?) | Scroll/Touch/Cursor MainNavigation window (icons?)						  |
| BaseBg.bflyt                 | BaseBackground                    | Contains a loading indicator for when the list is still loading                	  |
| BaseChild.bflyt		       | BaseChild (applet?)		       | Contains Basic Layout information for applet parts (header/side/main content)	  |
| BgNav_Root.bflyt	       | BackgroundNavigation_Root	       | Navigation Background Panel									  |
| BgNml.bflyt                  | BackgroundNormal                  | Contains mainmenu background pane + '[exelixbg](../../../definitions.md#exelixbg)' |
| BtnIslandIcon.bflyt          | ButtonIslandIcon		       | Button contents text color/icon (L R +)							  |
| BtnIslandNml.bflyt	       | ButtonIslandNormal		       | Standard Button information text color								  |
| BtnLineNml.bflyt	       | ButtonLineNormal			 | Button "inline" ie dropdown list?								  |
| BtnOpt_Root.bflyt	       | ButtonOption_Root			 | Button information in drop down? Contains checkbox invalid & valid inc mark	  |
| BtnExpand.bflyt              | ButtonExpand                      | Drop Down Menu [groups?/sort] possibly changed in 14.0                             |
| Cursor3.bflyt                | Cursor3                           | Cursor                                                                         	  |
| DBtmFlcSortAndFilter.bflyt   | BottomFullLauncherSortAndFilter   | contains the "sort and filter" menu base information					  |
| DBtmHeaderNml.bflyt	       | BottomHeaderNormal		       | Contains header information icon / text & top line						  |
| FlcBalloon.bflyt             | FullLauncherBalloon               | App name balloon 			                                                  |
| FlcBtnGrp.bflyt			 | FullLaunchButtonGroup		 | Group Icon with clustered Icon includes the sort allows / text				  |
| FlcBtnGrpBlock.bflyt		 | FullLaunchButtonGroupBlock		 | Group Icon block information scrolling/spacing of the 4 groupicon rows		  |
| FlcBtnIconGame.bflyt         | FullLauncherButtonIconGame        | The game icon layout. Used for all icons                                       	  |
| FlcBtnIconGameBlock.bflyt    | FullLauncherButtonIconGameBlock   | Game Icon information in Rows/padding                                         	  |
| FlcBtnIconGameEdit.bflyt	 | FullLaunchButtonIconGameEdit	 | Game Icon in edit screen (sort/move/check)							  |
| FlcBtnIconGameEditBlock.bflyt| FullLaunchButtonIconGameEditBlock | Edit Game Icon Layout Padding information							  |
| FlcBtnLineAddGrp.bflyt	 | FullLaunchButtonLineAddGroup	 | Create Group Button											  |
| FlcCntMain.bflyt		 | FullLauncherContentMain		 | The Main AllApps screen window									  |
| FlcDGrpDelete.bflyt		 | FullLaunchDialogGroupDelete 	 | "Delete Group" Applet layout information							  |
| FlcDGrpOption.bflyt          | FullLaunchDialogGroupOption	 | "Edit Group" drop down list information							  |
| FlcGrpList.bflyt		 | FullLaunchGroupList			 | Groups Main Window / Sort Groups Main Window (both layouts are in this window)	  |
| FlcGrpMain.bflyt		 | FullLaunchGroupMain			 | Group Folder Contents Window (icons in group folder)					  |
| FlcGrpSoftArrangement.bflyt  | FullLaunchGroupSoftwareArrangement| Sort Software Contents Window (Sort Games in a Group Folder)				  |
| FlcGrpSoftEdit.bflyt		 | FullLaunchGroupSoftwareEdit       | Add/Remove Software Contents Window (Add & remove/search games window)		  |
| LineHeader_Root.bflyt        | LineHeader Root                   | The horizontal line that is shown in the header (size & relative position)      	  |
| NtfBtnSearchChannel.bflyt    | NotificationButtonSearchChannel	 | "Search by Keyword" Box/button & magnifier icon						  |
| TextH1.bflyt                 | TextHeader1                       | The complete main header component                                                 |
| TextH2.bflyt			 | TextHeader2				 | Header Text within groups										  |
| Waitingicon.bflyt		 | WaitingIcon				 | Loading icon												  |

_Not finished yet_
