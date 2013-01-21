GeoFav
======

A mobile web app that spots the current location of a user giving the option to save it as a favorite one. This is achieved by invoking HTML5 Geolocation and Google Maps API.

<!--IMPORTANT-->

In order to make this app work create the above tables in your database. Either by MySQL query or via phpMyAdmin. 
Also fill in your settings inside "connect.php" file in order to connect the app with your database.

-- Table structure for table `usr`

CREATE TABLE `usr` (
  `id` int(50) NOT NULL AUTO_INCREMENT,
  `uname` varchar(50) CHARACTER SET utf8 NOT NULL,
  `pass` varchar(50) CHARACTER SET utf8 NOT NULL,
  `firstname` varchar(50) CHARACTER SET utf8 NOT NULL,
  `lastname` varchar(50) CHARACTER SET utf8 NOT NULL,
  `email` varchar(60) CHARACTER SET utf8 NOT NULL,
  `randsalt` varchar(50) CHARACTER SET utf8 NOT NULL,
  PRIMARY KEY (`id`),
  UNIQUE KEY `uname` (`uname`)
) ;

-- Table structure for table `place`

CREATE TABLE `place` (
  `plid` int(40) NOT NULL AUTO_INCREMENT,
  `plusrid` int(50) NOT NULL,
  `plname` varchar(50) CHARACTER SET utf8 NOT NULL,
  `pldesc` varchar(50) CHARACTER SET utf8 NOT NULL,
  `plcat` varchar(50) CHARACTER SET utf8 NOT NULL,
  `pldate` varchar(50) COLLATE latin1_general_ci NOT NULL,
  `pllat` float(10,6) NOT NULL,
  `pllon` float(10,6) NOT NULL,
  PRIMARY KEY (`plid`)
) ;
