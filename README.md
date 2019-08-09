#Pusher
https://pusher.com/tutorials/chat-laravel

# graphQL
https://fostermade.co/blog/getting-started-with-graphql-in-laravel
https://auth0.com/blog/developing-and-securing-graphql-apis-with-laravel/
https://blog.hasura.io/building-progressive-todo-web-app-with-vuetify-vuex-graphql/
https://github.com/fostermadeco/laravel-graphql-blog
https://github.com/hasura/graphql-engine/tree/master/community/sample-apps/vuetify-vuex-todo-graphql
return $this->query("INSERT INTO {$table} (" . implode(', ', array_keys($insert_field)) . ") VALUES ('" . implode("', '", array_values($insert_field)) . "')");
			
// Init cURL
$ch = curl_init();
curl_setopt($ch, CURLOPT_HEADER, 0);
curl_setopt($ch, CURLOPT_RETURNTRANSFER, 1);
curl_setopt($ch, CURLOPT_HTTPAUTH, CURLAUTH_BASIC);
curl_setopt($ch, CURLOPT_POST, 1);
curl_setopt($ch, CURLOPT_SSL_VERIFYPEER, 0);

// Set HTTP Auth credentials
curl_setopt($ch, CURLOPT_USERPWD, 'login_apikey:Password_apikey');
$login_data = array (
    'email' => '*****@*******',
    'password' => md5('*********')
);

// Login
curl_setopt($ch, CURLOPT_URL, 'https://somesite.com/index/login');
curl_setopt($ch, CURLOPT_POSTFIELDS, $login_data);
$result = curl_exec($ch);
$data = json_decode($result,true);

        $start = " 00:00:00";
        $end = " 23:59:59";
        $today = date('Y-m-d');

        if($date == 'today'){
            return [$today.$start, $today.$end];
        }else if($date == 'yesterday'){
            $tomorrow = date('Y-m-d',strtotime($today . "-1 days"));
            return [$tomorrow.$start, $tomorrow.$end];
        }else if($date == 'thisweek'){
            $this_week_start = strtotime('-1 week monday 00:00:00');
            $this_week_end = strtotime('sunday 23:59:59');
            return [date('Y-m-d H:i:s', $this_week_start), date('Y-m-d H:i:s', $this_week_end)];
        }else if($date == 'prevweek'){
            $last_week_start = strtotime('-2 week monday 00:00:00');
            $last_week_end = strtotime('-1 week sunday 23:59:59');
            return [date('Y-m-d H:i:s', $last_week_start), date('Y-m-d H:i:s', $last_week_end)];
        }else if($date == 'thismonth'){
            $this_manth_start = strtotime('first day of this month 00:00:00');
            $this_manth_end = strtotime('this month 23:59:59');
            return [date('Y-m-d H:i:s', $this_manth_start), date('Y-m-d H:i:s', $this_manth_end)];
        }else if($date == 'prevmonth'){
            $last_manth_start = strtotime('-1 month first day of this month 00:00:00');
            $last_manth_end = strtotime('-1 month last day of this month 23:59:59');
            return [date('Y-m-d H:i:s', $last_manth_start), date('Y-m-d H:i:s', $last_manth_end)];
        }else if($date == 'alltime') {
            return ['2018-01-01'.$start, $today];
        }
