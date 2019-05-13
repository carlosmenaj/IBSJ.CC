$url = 'URL';
        $tag = 'Tag';
        $id = 'P_Id';

        $query = "SELECT * FROM web_db WHERE Tag = '" . $userTag . "' ORDER BY RAND() LIMIT 1";

        $result = mysql_query($query);
        if($result) 
        {
            while($row = mysql_fetch_array($result))
           {
              echo 'ID:' . $row[$id] . '<br>';
              echo 'URL: ' . $row[$url] . '<br>';
              echo 'Tag:' . $row[$tag] . '<p>';


        //    $remote = fopen($row[$url],"r");
        //    fpassthru($remote);

            echo '<iframe src="'.$row[$url].'" width="100%" />';
