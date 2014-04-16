Basic-Java
==========

Sorting

        public static <T extends Comparable<T>> void printSorted(ArrayList<T> list)
        {
              ArrayList<T> sortedList = (ArrayList<T>) list.clone();
            boolean swapped = true;
            while(swapped){
                swapped = false;
                for(int i = 0; i < sortedList.size()-1; i++)
                {
                    if((sortedList.get(i)).compareTo(sortedList.get(i+1)) > 0)
                    {
                        T higher = sortedList.get(i);
                        T lower = sortedList.get(i+1);
                        sortedList.remove(i);
                        sortedList.remove(i);
                        sortedList.add(i,lower);
                        sortedList.add(i+1, higher);
                        swapped = true;
                    }
                }
            }
            System.out.print(sortedList);

