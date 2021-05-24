/*!40101 SET NAMES utf8 */;

/*!40101 SET SQL_MODE=''*/;

/*!40014 SET @OLD_UNIQUE_CHECKS=@@UNIQUE_CHECKS, UNIQUE_CHECKS=0 */;
/*!40014 SET @OLD_FOREIGN_KEY_CHECKS=@@FOREIGN_KEY_CHECKS, FOREIGN_KEY_CHECKS=0 */;
/*!40101 SET @OLD_SQL_MODE=@@SQL_MODE, SQL_MODE='NO_AUTO_VALUE_ON_ZERO' */;
/*!40111 SET @OLD_SQL_NOTES=@@SQL_NOTES, SQL_NOTES=0 */;

CREATE DATABASE /*!32312 IF NOT EXISTS*/`employeeManagement` /*!40100 DEFAULT CHARACTER SET utf8mb4 */;

USE `employeeManagement`;

/*Table structure for table `Employee` */

DROP TABLE IF EXISTS `Employee`;

CREATE TABLE `Employee` (
  `EmployeeID` int(11) NOT NULL,
  `FirstName` varchar(50) NOT NULL,
  `LastName` varchar(50) NOT NULL,
  `City` varchar(50) NOT NULL,
  `State` varchar(50) DEFAULT NULL,
  PRIMARY KEY (`EmployeeID`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;

/*Data for the table `employee` */

insert  into `Employee`(`EmployeeID`,`FirstName`,`LastName`,`City`,`State`) values 

(10330,'John','John','NY','NY'),
(10449,'Sarah','Lebat','Melbourne','Bourke'),
(11012,'Jon','Dallas','NY','NY'),
(11013,'Gheorhe','Honey','NY','NY'),
(11014,'Anton','Savar','NY','NY');


/*Table structure for table `Payments` */

DROP TABLE IF EXISTS `Payments`;

CREATE TABLE `Payments` (
  `EmployeeID` int(11) NOT NULL,
  `SalaryDate` varchar(50) NOT NULL,
  `MounthID` int(11) NOT NULL,
  `Value` int(11) NOT NULL,
  CONSTRAINT `Payments_ibfk_1` FOREIGN KEY (`EmployeeID`) REFERENCES `Employee` (`EmployeeID`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;

/*Data for the table `Payments` */

insert  into `Payments`(`EmployeeID`,`SalaryDate`,`MounthID`,`Value`) values 

(10330,'June',6,128),
(10330,'July',7,158),
(10330,'August',8,133),
(10330,'September',9,120),
(10330,'October',10,188),
(10330,'November',11,160),
(10330,'December',12,105),
(10449,'September',9,150),
(10449,'October',10,158),
(10449,'November',11,160),
(10449,'December',12,180);
