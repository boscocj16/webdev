const Header = ({ course }) => {
  return <h1>{course}</h1>;
};

export default Header;



const Content = ({ part1, exercises1, part2, exercises2, part3, exercises3 }) => {
  return (
    <div>
      <p>{part1} {exercises1}</p>
      <p>{part2} {exercises2}</p>
      <p>{part3} {exercises3}</p>
    </div>
  );
};

export default Content;


const Total = ({ exercises1, exercises2, exercises3 }) => {
  return <p>Number of exercises {exercises1 + exercises2 + exercises3}</p>;
};

export default Total;


import Header from './header';
import Content from './content';
import Total from './total';
