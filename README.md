TASK DATE: 18.10.2017

TASK SHORT DESCRIPTION: 1150 ('use my profile address' bug)

GITHUB REPOSITORY CODE: hotfix/task-1150-use-my-profile-address

ORIGINAL WORK: https://github.com/BusinessBecause/network-site/tree/hotfix/task-1150-use-my-profile-address

CHANGES AND ADDED CODES
  - system didn't give address details to the imput fields
	  caused: record in the 'default_profiles_address' table, fields with NULL values

  - sql query problem
  	caused: non-exist 'ship_to_profile_address' table field in 'default_profiles_address' table 
  	network-site\addons\default\modules\firesale\models\address_m: 
	  	//added extra ignoring input field: ship_to_profile_address
	  	line 100: $ignore = array('shipping', 'ship_to', 'bill_to', 'ship_to_user', 'bill_to_user', 'ship_to_profile_address');
