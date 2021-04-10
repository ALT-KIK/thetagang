All the main work/code is located in the thetagang file. Inside here thare are 11 files. 

thetagang/__init__.py - empty file.

Interace and configurations were made by using thetagang/config.py and thetagang/thetagang.py files. There thetagang/config_defaults.py gives default values of configurations to the thetagang/config.py. These are used by using click library, which is used mainly to build interaces by proving UI elements. In the thetagang/config.py the default values from the thetagang/config_defaults.py are applied by using the apply_default_values method, which uses dict_merge method that is implemented in thetagang/dict_merge.py. The main work in thetagang/config.py is made in validate_config method. The project's interface is made in the terminal. As written above, the interface is mainly implemented in thetagang/thetagang.py. 

The thetagang/dict_merge.py has one method only which is dict_merge method. This method is used to update keys by recursing down into dictionary's nested
to an arbitrary depth. This method is used in other files such as thetagang/config.py.


thetagang/main.py - main entry point here. It starts the application.

thetagang/options.py contatins two methods wich are: contract_date_to_datetime and option_dte. These methods are used to set a timer for the usage. contract_date_to_datetime method is setting the expiration date, where option_dte methods is used to calculate the duration of the contract itself. 

thetagang/portfolio_manager.py is used mainly for operations on puts and calls. This file is used to getting the puts and calls, putting them, rolling them where the check before whether puts and calls can be rolled should be done. Also checking the puts and calls, writing them is done by the thetagang/porfolio_manager.py. Also these can be filtered. The other work than operations on puts and calls, this file is used to initializng, summarizing and managing the account. In addition it is used to submit the trade and before doing so it also checks if it is possible or not. All this work should be done by finding the appropriate contracts. 


There is also thetagang/util.py, which contains some useful methods such as:  to_camel_case, account_summary_to_dict, portfolio_positions_to_dict, justify, position_pnl, while_n_times, midpoint_or_market_price and get_target_delta. to_camel_case method is used to convert the the string to the camel case. account_summary_to_dict is used to convert the account summary to the dictionary. portfolio_postitions_to_dict also used to convert the porfolio positions to the dictionary. justify method is for justifying to the right by 12. And get_target_delta is used to get the target delta. Other methods are also intuitivly identified by their names. 













