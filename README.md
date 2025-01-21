import Header from './header';
import Content from './content';
import Total from './total';




const Part = ({ partName, exercises }) => {
  return (
    <p>{partName} {exercises}</p>
  );
};

export default Part;


import Part from './part';

const Content = ({ part1, exercises1, part2, exercises2, part3, exercises3 }) => {
  return (
    <div>
      <Part partName={part1} exercises={exercises1} />
      <Part partName={part2} exercises={exercises2} />
      <Part partName={part3} exercises={exercises3} />
    </div>
  );
};

export default Content;
