<?php
$secret_key = "DaddyOllieman"; //Set this as your secret key, to prevent others uploading to your server.
$sharexdir = "https://fuckniggers.lol/ss/"; //This is your file dir, also the link..
$domain_url = 'https://fuckniggers.lol/';
$lengthofstring = 4; //Length of the file name

function RandomString($length) {
    $keys = array_merge(range(0,9), range('a', 'zslow

    $key = '';
    for($i=0; $i < $length; $i++) {
        $key .= $keys[mt_rand(0, count($keys) - 1)];
    }
    return $key;
}
$filename = RandomString($lengthofstring);
$target_file = $_FILES["DaddyOllieman"]["name"];
$fileType = pathinfo($target_file, PATHINFO_EXTENSION);

if (move_uploaded_file($_FILES["DaddyOllieman"]["tmp_name"], $sharexdir.$filename.'.'.$fileType)) 
{
    echo $domain_url.$sharexdir.$filename.'.'.$fileType;
}
    else
{
   echo 'File upload failed - CHMOD/Folder doesn\'t exist?';
}
?>
