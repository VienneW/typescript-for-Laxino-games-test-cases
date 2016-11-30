# typescript-for-Laxino-games-test-cases
Testcases are more less the same, but the GameBook API for Laxino games is a bit different, the post body format is application/x-www-form-urlencoded


the API call is like this:
```
bet_async = (json) => {

        let body_url_encoded = "login_name=" + json.login_name + "&session_token=" + json.session_token + "&bet_amt=" + json.bet_amt + "&ref_trans_id=" + json.ref_trans_id + "&round_id=" + json.round_id + "&game_id=" + json.game_id + "&trans_date=" + json.trans_date ;
        
        let option = {
            method: "POST",
            url: this.url + "/bet",
            qs: {
                cage_id: json.cage_id,
                debugger: 1
            },
            body: body_url_encoded,
            json: true,
            headers: {
                "content-Type": "application/x-www-form-urlencoded",
                "Date": json.date
            }
        }
        console.log("********** bet_async INPUT ********** \n", option)
        console.log("")
        return rp(option);
    }
```

references:

// date format
https://www.npmjs.com/package/date-and-time

// post body: replace spaces with %20, replace + sign with %2B
http://stackoverflow.com/questions/2678551/when-to-encode-space-to-plus-or-20






